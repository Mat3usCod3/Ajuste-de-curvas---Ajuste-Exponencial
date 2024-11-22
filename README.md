# Ajuste de Curvas - Ajuste Exponencial

Este notebook contém uma implementação para ajuste exponencial de dados, utilizando Python. O ajuste exponencial é uma técnica de modelagem utilizada para analisar fenômenos de crescimento ou decaimento exponenciais.

## Métodos e Funções

### 1. `grafico()`

**Objetivo**: Este método é utilizado para gerar um gráfico que exibe os dados de entrada. O gráfico ajuda a visualizar o comportamento dos dados e a verificar se eles seguem uma tendência exponencial.

#### Parâmetros:
- `dados` (array-like): Um conjunto de dados, com as variáveis independentes $x$ e dependentes $y$.

#### Como utilizar:
```python
grafico(dados)
```

### 2. `ajustar()`

**Objetivo**: Este método ajusta uma curva exponencial aos dados fornecidos, utilizando um algoritmo de otimização. Ele retorna os coeficientes da função ajustada, bem como o coeficiente de determinação $R^2$, que indica a qualidade do ajuste.

#### Parâmetros:
- `dados` (array-like): Um conjunto de dados $x, y$ que será ajustado à curva exponencial.

#### Retorno:
- Um dicionário contendo:
  - `coeficientes`: Os coeficientes $a$ e $b$ da função exponencial ajustada.
  - `R2`: O valor do coeficiente de determinação, que indica a precisão do ajuste.

#### Como utilizar:
```python
resultados = ajustar(dados)
print(resultados)
```

### 3. `interpolar()`

**Objetivo**: Este método calcula o valor de $y$ para um ou mais valores de $x$, utilizando os coeficientes da curva exponencial ajustada.

#### Parâmetros:
- `x` (float ou array-like): O valor de $x$ ou uma lista de valores $x$ para os quais você deseja estimar os valores de $y$.
- `coeficientes` (tuple): Os coeficientes $a$ e $b$ da curva exponencial ajustada.

#### Retorno:
- O valor de $y$ estimado, ou uma lista de valores estimados de $y$ para múltiplos valores de $x$.

#### Como utilizar:
```python
y_estimado = interpolar(10, resultados['coeficientes'])
print(y_estimado)
```

---

## Exemplo de Uso

Aqui está um exemplo simples de como utilizar os métodos do notebook:

```python
# Dados de exemplo
dados = [[1, 2, 3, 4], [2.7, 7.4, 20.1, 54.6]]

# Visualizar os dados
grafico(dados)

# Ajustar a curva exponencial
resultados = ajustar(dados)
print(resultados)
# Saída esperada: {'coeficientes': (2.0, 0.7), 'R2': 0.98}

# Interpolar para um valor de x
y_estimado = interpolar(5, resultados['coeficientes'])
print(y_estimado)
# Saída esperada: 147.0
```

---

Este notebook permite ajustar dados a uma curva exponencial e realizar previsões com base no modelo ajustado. A função `grafico()` é útil para validar visualmente a relação dos dados, enquanto os métodos `ajustar()` e `interpolar()` permitem calcular o melhor ajuste e realizar previsões, respectivamente.

Se desejar mais detalhes ou alterações na documentação, estou à disposição para ajustar! 😊

