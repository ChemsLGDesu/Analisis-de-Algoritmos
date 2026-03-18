# Analisis-de-Algoritmos
1._

int SumScores (int [] scores)               // scores seria mi N
{
  int sum = 0;                             // Aqui seria 1 porque es una asignación 
  for (int i = 0; i < scores.Length; i++)  // +1 (init) + (N+1 Comparaciones)   + N incrementos
  {
      sum += scores [i];                   // una asignacion doble que es el (+=) 2 + N 
  }

  return sum;                              // +1
}

Procedimiento: T(M) = 1+1+(N+1)+N+2+N+1
               T(M) = 3N+6
               O(n) = N

2._
