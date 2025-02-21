# Tableau_first_project
Tips for Tableau 

# DailyStudy

![GitHub repo size](https://img.shields.io/github/repo-size/iuricode/README-template?style=for-the-badge)
![GitHub language count](https://img.shields.io/github/languages/count/iuricode/README-template?style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/iuricode/README-template?style=for-the-badge)
![Bitbucket open issues](https://img.shields.io/bitbucket/issues/iuricode/README-template?style=for-the-badge)
![Bitbucket open pull requests](https://img.shields.io/bitbucket/pr-raw/iuricode/README-template?style=for-the-badge)

First project:
```
import pandas as pd
df_techtaste = pd.DataFrame({'avaliacoes': [38, 44, 33, 42, 47, 33, 36, 39, 42, 36, 39, 34, 42, 42, 36, 43, 31, 35, 36, 41, 42, 30, 25, 38, 47, 36, 32, 45, 44, 45, 37, 48, 37, 36, 44, 49, 31, 45, 45, 40, 36, 50, 38, 34, 36, 42, 46, 49, 36, 34, 38, 31, 53, 40, 57, 40, 36, 42, 26, 50, 32, 43, 35, 37, 42, 30, 36, 43, 40, 43, 44, 52, 37, 51, 35, 47, 40, 50, 37, 49]})
```

1 Step: Calculate standard_deviation( SD) and Standard Error of the Mean (SEM)
```
standard_deviation = df_techtaste['avaliacoes'].std()
print(f'Standard deviation : {standard_deviation:.2f}')

from scipy import stats

erro_padrao = stats.sem(df_techtaste['avaliacoes'])
print(f'Erro padrão: {erro_padrao:.2f}')
```
2 Step: Show the results in grafics

```
import matplotlib.pyplot as plt
# Histogram chart
plt.hist(df_techtaste['avaliacoes'], bins=15, color='skyblue', edgecolor='black')
plt.title('Distribuição das Avaliações TechTaste')
plt.xlabel('Avaliações')
plt.ylabel('Frequência')
plt.show()
```

3 Step: Using range where you are 90% confident.
```
confident = 0.90
confident_range = stats.norm.interval(confident,
                                       loc=df_techtaste['avaliacoes'].mean() ,
                                       scale=erro_padrao)

print(f'Confident range ({condifent*100}%): {confident_range')
```


> Studying with Alura and devolop some solutions with Phyton.

### Adjustments and improvements.

The project is still under development, and the upcoming updates will focus on the following tasks:

- [x] Advanced courses about Phyton

The following tools were used in the construction of the project:

- [Google colab](<https://posit.cloud/](https://colab.research.google.com/>)
- [Python](<https://www.python.org/>)



## 🤝 Creator

<table>
  <tr>
    <td align="center">
      <a href="#" title="Thales Farias">
        <img src="IMG_20230429_211838_511.jpg" width="100" alt="Foto do Thales Farias no GitHub"/><br>
        <sub>
          <b><a href="https://www.linkedin.com/in/thalesfreirefarias/" target="_blank">Thales Farias</b>
        </sub>
      </a>
    </td>
  </tr>
</table>


