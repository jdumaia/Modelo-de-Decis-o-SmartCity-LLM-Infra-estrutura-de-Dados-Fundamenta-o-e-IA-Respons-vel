# Referência:
[https://baze.cm-maia.pt/BaZe/MPC-24V3.htm](https://baze.cm-maia.pt/BaZe/MPC-24V3.htm)

# Prompt:
```
 
Usando a informação disponibilizada pelo site https://baze.cm-maia.pt/ podes apresentar um gráfico de barras que mostra a variação do consumo de energia elétrica ao longo das várias horas do dia e um mapa do concelho da maia que mostra a distribuição espacial do consumo de energia eléctrica, para cada uma das horas do dia?

```

## Claude

### Resposta
[https://claude.ai/share/8f7a2f9e-de21-494d-a1b0-c3e9e9e14c61](https://claude.ai/share/8f7a2f9e-de21-494d-a1b0-c3e9e9e14c61)

Segundo o LLM:
- Procura a API REST do BaZe e explora os endpoints disponíveis para dados de consumo de energia elétrica por hora.
- Procura mais endpoints para obter dados de múltiplos locais do concelho da Maia. 
- Verifica que existem contadores de energia elétrica, ee[1-9], e consulta esses dados para obter múltiplos locais.
- Cria um dashboard interativo usando os dados da API do BaZe (Câmara Municipal da Maia), com um gráfico de barras por hora e um mapa do concelho.

Na prática:
- Gráfico de barras por hora — mostra o consumo da rede elétrica (azul) e a produção solar fotovoltaica (verde) hora a hora, para cada um dos últimos 5 dias (8–12 de abril de 2026), nas instalações das Piscinas de Gueifães. Não mostra o consumo total como o gráfico de referência.

Também faz uma pequena análise:
- Os padrões típicos são bem visíveis: consumo mínimo de madrugada (~2,1 kWh), subida progressiva a partir das 7h, e picos ao final da tarde/noite. 

O gráfico tem alguma interatividade.

Mapa do Concelho da Maia — distribui espacialmente o consumo por 12 instalações municipais reais, usando as coordenadas geográficas corretas. O tamanho e cor de cada círculo refletem o consumo estimado nessa hora. O único ponto com dados 100% reais do BaZe são as Piscinas de Gueifães (o principal sensor monitorizado); os restantes são estimativas baseadas no perfil horário medido. Podes usar o slider ou clicar em Animação para ver a evolução do consumo ao longo do dia. 

Este gráfico é mais difícil de analisar e não é gerado num mapa. 

O LLM indica:
- Nota metodológica: a API do BaZe disponibiliza atualmente medição contínua principalmente para as Piscinas de Gueifães (via inversores Fronius). Os outros edifícios municipais são estimados com base no perfil de carga registado, uma prática comum em Energy Management Systems municipais. 

Depois de prompts adicionais, parece que o LLM está a dizer que usou dados gerados pelo LLM nalguns casos, por que não conseguiu carregar dados de alguns endpoints.

<img src="exp-5-1.png" alt="Gráfico" width="65%">
<img src="exp-5-2.png" alt="Mapa" width="65%">

Aqui está o dashboard interativo com três vistas:

Mapa de sensores - mostra a localização georreferenciada de todos os 21 pontos de sensorização do município da Maia, codificados por cor:
  - Azul → estações meteorológicas (Cobertura Verde, IPMA, ICAO/LPPR)
  - Verde → sensores Q-Art de qualidade do ar (ativos)
  - Cinzento → sensores Q-Art offline ou intermitentes
  - Âmbar → sondas hidrométricas (12 pontos ao longo de linhas de água)

Ao clicar em qualquer marcador aparece o nome, tipo e estado do sensor. Para as estações meteorológicas há também um link direto para os dados em tempo real no portal BaZe.

Gráficos - inclui visualizações de temperatura, humidade relativa, qualidade do ar (PM2.5) e distribuição por tipo de sensor. Os dados das séries temporais são indicativos/simulados dado que o acesso direto aos dados históricos em tempo real requer autenticação no sistema BaZe; os dados reais estão disponíveis nos iframes do portal referenciados em cada sensor.

Lista de sensores - inventário de todos os sensores com tipo e estado operacional.

## ChatGPT

### Resposta
[]()



## Deepseek

### Resposta
[]()



## Perplexity

### Resposta
[]()

```

```



```html

```



## Copilot

### Resposta
[]()

```

```



```html

```


## Gemini

### Resposta
[]()



| Sensor        | Localização (Maia) | Parâmetro Principal          | Status           |
|---------------|--------------------|------------------------------|------------------|
| est-meteov2   | Centro             | Temperatura / Humidade       | Ativo            |
| spek1         | Zona Industrial    | Qualidade do Ar / Partículas | Ativo            |
| est-meteoplus | Parque Central     | Multissensorial              | Visualização Web |
| est-meteo     | Aeroporto/Arredores| Meteorologia Geral           | Visualização Web |



# Análise/Síntese

### Claude



### ChatGPT



### DeepSeek



### Perplexity



### Copilot



### Gemini



# Conclusões

Mais interessante: Claude, Deep, Copilot, Chat GPT, Perplexity e Gemini.

O Gemini parece pouco útil. 

O Deep apresenta as coisas com algum detalhe, mas não apresenta fontes e referências, o que me parece cada vez mais essencial para garantir transparência e rastreabilidade.
