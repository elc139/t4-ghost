# T4: Simulador de Propagação de Vírus com OpenMP
Alexandre Moreira Medina - ELC139

# Soluções

[Solução 1](omp_virusim) - Paralelizar a região onde é executada os n experimentos, definindo como privada o objeto que manipula a população. Para garantir que nenhum resultado seja alterado devido a condição de corrida, na variável percent_infected foi utilizado exclusão mútua.

[Solução 2](omp_virusim_2) - Paralelizar o loop de probabilidades, utilizando um vetor de População, para que cada thread manipule uma população separada uma da outra, fazendo com que o uso de exclusão mútua não seja necessária em nenhuma parte do loop.


# Resultados
[Slides](slides.pdf)

# Referências

- [Parallel Region](https://computing.llnl.gov/tutorials/openMP/#ParallelRegion)
- [OpenMP: For & Scheduling](http://jakascorner.com/blog/2016/06/omp-for-scheduling.html)