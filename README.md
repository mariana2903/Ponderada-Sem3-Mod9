# Ponderada-Sem3-Mod9

## Relatório de Testes de Unidade em C#

Nesse exercício foi feito a criação, execução e personalização de alguns testes de unidade, usando a tecnologia e estrutura de teste de unidade da microsoft para código gerenciado e gerenciador de testes da do Visual Studio.

Nesse processo foi construído um código e testes que exercitam o código, e durante o processo até o resultado final o código os testes passaram por algumas mudanças e depois foram novamente executados.
Realizando um passo a passo de como foi o processo de realização da atividade, primeiro foi criado a lógica do código, que representa uma conta bancária, e que depois seria testado. Depois, foi criado o projeto de teste de unidade, o projeto de teste de unidade do MSTest em C# também, como o restante do código, nele foram adicionados alguns testes. 

A classe de teste deve seguir certos requisitos para ser reconhecida pelo Gerenciador de Testes:

- A classe deve ser decorada com o atributo [TestClass].
- Cada método de teste deve ser decorado com o atributo [TestMethod].

Em seguida os testes, o primeiro verifica que um valor válido, ou seja, menor que o saldo da conta e maior que zero, retira a quantidade correta da conta. O método é simples: ele define um novo objeto `BankAccount` com um saldo inicial e, em seguida, retira um valor válido. Ele usa o método [Assert.AreEqual] para verificar se o saldo final é conforme o esperado. Métodos como `Assert.AreEqual`, [Assert.IsTrue] e outros são frequentemente usados em testes de unidade.
Esse teste inicialmente falha e é necessário corrigir o código, substituindo uma linha:

m_balance += amount;  por  m_balance -= amount; 

e depois o teste é executado com sucesso.

O segundo, verifica o comportamento correto quando o valor do débito é menor que zero, usando o método  [ThrowsException] para declarar que a exceção correta foi gerada. Esse método faz com que o teste falhe, a menos que uma [ArgumentOutOfRangeException] seja gerada. 

Depois é feito terceito teste semelhante ao segundo, mas ao invés de `Debit_WhenAmountIsMoreThanBalance_ShouldThrowArgumentOutOfRange`é `Debit_WhenAmountIsLessThanZero_ShouldThrowArgumentOutOfRange`

Por fim feita uma última refatoração do código em teste e dos testes, que são executados novamente e por fim todos passam. 

A conclusão portanto, as melhorias no código de teste levaram a métodos de teste mais robustos e informativos. Porém, o mais importante é que eles também melhoraram o código em teste.

Alguns conceitos aprendidos durante o exercício, e diversos conceitos fundamentais foram reforçados de módulos anteriores:

- Desenvolvimento orientado a testes (TDD): A prática de escrever testes antes mesmo do código que será testado.
- Asserts: A utilização de assertivas para validar o comportamento do código.
- Refatoração: O processo de modificar um código-fonte existente para melhorar sua estrutura e legibilidade, sem alterar seu comportamento externo.
- Tratamento de exceções: A importância de gerenciar corretamente as exceções que o código pode lançar.

  ## Resultado Final do código em execução



