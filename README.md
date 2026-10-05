# 📊 Simulador de Investimentos em Fundos Imobiliários (FIIs)

Ferramenta desenvolvida em Microsoft Excel para simular acumulação de património e geração de rendimento passivo mensal com Fundos de Investimento Imobiliário (FIIs), adaptando a carteira ao perfil de risco do investidor.

---

## 🎯 As Cinco Perguntas que a Ferramenta Responde

Na aba **APP**, a ferramenta recolhe os parâmetros do utilizador e responde directamente às seguintes questões:

1. **Quanto posso investir por mês com base no meu salário?**
   * *Onde aparece:* Célula `D16` (Sugestão de Investimento), calculando uma margem prudencial de 30% sobre a receita mensal.
2. **Quanto vou investir por mês?**
   * *Onde aparece:* Célula `D19`, definindo o aporte regular mensal.
3. **Por quantos anos o dinheiro vai render?**
   * *Onde aparece:* Célula `D20`, determinando o horizonte temporal da estratégia.
4. **Qual é o património acumulado no fim do período?**
   * *Onde aparece:* Célula `D22` (Património acumulado?), aplicando capitalização composta sobre os aportes.
5. **Quanto receberei de dividendos mensais?**
   * *Onde aparece:* Célula `D23` (Dividendos Mensais?), demonstrando a renda passiva estimada gerada pelo património acumulado.

---

## 🧮 Lógica das Fórmulas: VF e PROCV

### 1. Função VF (`FV` - Valor Futuro)
Utilizada para calcular o património acumulado em juros compostos:
```excel
=FV(taxa_mensal; qtd_anos*12; aporte*-1)
