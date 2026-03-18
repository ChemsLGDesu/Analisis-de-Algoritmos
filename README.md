# Analisis-de-Algoritmos
1._

int SumScores (int [] scores)               // scores seria mi N
{
  int sum = 0;                             // Aqui seria 1 porque es una asignación 
  for (int i = 0; i < scores.Length; i++)  // +1 (init) + (N+1 Comparaciones)   + N de incrementos
  {
      sum += scores [i];                   // una asignacion doble que es el (+=) 2 + N 
  }

  return sum;                              // +1
}

Procedimiento: T(M) = 1+1+(N+1)+N+2+N+1
               T(M) = 2+(N+1)2N+3
               T(M) = (N+1)+2N+5
               T(M) = 3N+5+1
               T(M) = 3N+6
               
               O(N) = N

-------------------------------------------------------------------------------------------------------------------------------------------------------

2._

void ComparePlayers(List<GameObject> players)      // players seria mi N
{
  for (int i = 0; i< players.Count; i++)           // +1 (init i) + (N+1 Comparaciones) + N de incrementos
  {
    for(int j = i+1; jj<players.Count; ++)         // +1 (init j)+N(i) +1(operacion aritmetica) + (N+1 Comparaciones) + N de incrementos
    {
      Debug.Log(players[i].name + "vs" + _________);  //+1 del (Debug.Log) + N (accediendo a una coleccion de players) +1 (operacion aritmetica) +1 (operacion aritmetica)
    }
  }
}
                   Interior del for                              Exterior del for
Procedimiento:   T(M) = 1+N+1+(N+1)+N+1+N+1+1              T(M) = 1+(N+1)+N+4N²+6N
                 T(M) = 1+N+1+(N+1)+N+N+3                  T(M) = 4N²+8N + 2
                 T(M) = N(4N +6)
                 T(M) = 4N²+6N
                                                          RPTA: T(M) = 4N²+8N + 2      O(N) = N²
-------------------------------------------------------------------------------------------------------------------------------------------------------
3._

int CalculateInteractionScore(int[] players)           // players seria mi N
{
  int score = 0;                                      // +1 (int)

  for( int i = 0; i < players.Length; i++)            // +1 (int) + (N+1 Comparaciones)+ N de incrementos
  {
    for( int j = i + 1; j < players.Length; j++)      // +1 (int) + (N+1 Comparaciones)+ N de incrementos
    {
      int interaction = players[i] + players[j];      // +1 (asignacion) + N + N (accede a la lista i y j de players)
      score += interaction;                           // +2 (asignacion)
    }
  
  }

  return score;                                      // +1 (score)
}
                       Interior del for                           Exterior del for
Procedimiento:      T(M) = 1+N+1+N+1+N+1+N+2                  T(M) = 1+1+N+1+N+4N²+6N+1
                    T(M) = 4N+6                               T(M) = 4N²+8N+4
                    T(M) = N(4N+6)
                    T(M) = 4N²+6N

---------------------------------------------------------------------------------------------------------------------------------------------------------

4._

int Calculate







