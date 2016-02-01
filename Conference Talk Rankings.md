
<div style="background-color:#000"> 
    <img src='https://raw.githubusercontent.com/leriomaggio/pycon7-community-voting/master/logos/pycon7.png' width='50%' />
</div>


```python
import pandas as pd
```

# Community Voting Results

### Absolute Ranking


```python
rankings = pd.read_csv('./ranking.txt', sep=' - ', engine='python', skiprows=1, 
                       names=('talk_id', 'type', 'track', 'lang', 'title', 'speaker'), 
                       index_col=0)
rankings.drop('talk_id', axis=1, inplace=True)

rankings
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>type</th>
      <th>track</th>
      <th>lang</th>
      <th>title</th>
      <th>speaker</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Gestione di errori ed eccezioni in Python 2 e ...</td>
      <td>Alex Martelli</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Training</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Beautiful async code in Python 3</td>
      <td>Anton Caceres</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Training</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Docker: dalla build a production</td>
      <td>Davide Setti</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Domotica a cinque euro con Raspberry Pi Zero e...</td>
      <td>Anna Chiara Bellini</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Exception and error handling in Python 2 and P...</td>
      <td>Alex Martelli</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Capire i Decoratori</td>
      <td>Ezio Melotti</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Ripensare la programmazione: un approccio funz...</td>
      <td>Francesco Bruni</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Delivery isn't magic anymore: distribuisci le ...</td>
      <td>Alan Franzoni</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>it</td>
      <td>Reti Neurali in Python</td>
      <td>Simone Piunno</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Mischiare threads e fork sotto unix: cose da f...</td>
      <td>Enrico Franchi</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Big data con PostgreSQL</td>
      <td>Giuseppe Broccolo</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>en</td>
      <td>Dockerizing Django projects</td>
      <td>Roberto Rosario</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Continuous delivery of a Python web project wi...</td>
      <td>Joost Cassee</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>$5 Home Automation with Raspberry Pi Zero and ...</td>
      <td>Anna Chiara Bellini</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>en</td>
      <td>Time Travel and Time Series Analysis with pand...</td>
      <td>Alexander Hendorf</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Training</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Computer Graphics per aspiranti game-developer...</td>
      <td>Roberto De Ioris</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>EuroCotoletta 2017</td>
      <td>Christian Barra</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Mixing multiprocessing and threads in the UNIX...</td>
      <td>Enrico Franchi</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Introduction of aiohttp</td>
      <td>Andrew Svetlov</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Understanding Decorators</td>
      <td>Ezio Melotti</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Building an asynchronous websocket server</td>
      <td>Tatiana Al-Chueyr</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>La vita di uno sviluppatore di free software</td>
      <td>Riccardo Magliocchetti</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Abstract Base Classes: un uso intelligente del...</td>
      <td>Leonardo Giordani</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Strings don't exist</td>
      <td>Martin Matusiak</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Tox as project descriptor: not only Continuous...</td>
      <td>Roberto Polli</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Ansible: automazione IT vocata al Cloud</td>
      <td>Ivan Rossi</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Comando di un robot con Python</td>
      <td>Antonio Spadaro</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>en</td>
      <td>Building Data Pipelines in Python</td>
      <td>Marco Bonzanini</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>en</td>
      <td>%%async_run: an IPython notebook magic for asy...</td>
      <td>Valerio Maggio</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Pglogical: il futuro della replica con Postgres</td>
      <td>Marco Nenciarini</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>83</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>it</td>
      <td>Aiuto !!! Ho un dataset "squilibrato" !</td>
      <td>Christian Barra</td>
    </tr>
    <tr>
      <th>84</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Autocompletamento per Blender Game Engine logic</td>
      <td>Anna Chiara Bellini</td>
    </tr>
    <tr>
      <th>85</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>it</td>
      <td>Introduzione a Orange Data Mining</td>
      <td>Eric Bonfadini</td>
    </tr>
    <tr>
      <th>86</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Python come Hardware Description Language</td>
      <td>Paolo Guadagnuolo</td>
    </tr>
    <tr>
      <th>87</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Progetti acceptance test-driven con Django</td>
      <td>Peter Bittner</td>
    </tr>
    <tr>
      <th>88</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Fate RPG: una web application per giocarlo onl...</td>
      <td>Saverio Porcari</td>
    </tr>
    <tr>
      <th>89</th>
      <td>Training</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Dive into object-oriented Python</td>
      <td>Leonardo Giordani</td>
    </tr>
    <tr>
      <th>90</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>From Java to Python</td>
      <td>OFFER SHARABI</td>
    </tr>
    <tr>
      <th>91</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Monitoraggio delle Risorse con Zabbix e Python</td>
      <td>Massimiliano Cuzzoli</td>
    </tr>
    <tr>
      <th>92</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Django e frontend? Gulp! Razionalizzare la ges...</td>
      <td>Alberto Motta</td>
    </tr>
    <tr>
      <th>93</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>it</td>
      <td>In-Database analytics with python and monetdb</td>
      <td>Danilo Maurizio</td>
    </tr>
    <tr>
      <th>94</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>it</td>
      <td>Lezioni devops per data scientist</td>
      <td>Luca Mearelli</td>
    </tr>
    <tr>
      <th>95</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>en</td>
      <td>Acceptance Test-driven Projects With Django</td>
      <td>Peter Bittner</td>
    </tr>
    <tr>
      <th>96</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Come passare indenni (o quasi) la traversata d...</td>
      <td>Ugo Scaiella</td>
    </tr>
    <tr>
      <th>97</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Blender Game Engine logic and autocompletion</td>
      <td>Anna Chiara Bellini</td>
    </tr>
    <tr>
      <th>98</th>
      <td>Training</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Rendi scalabile la tua app django</td>
      <td>Marco Paolini</td>
    </tr>
    <tr>
      <th>99</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Viaggiare leggeri col proprio progetto Django</td>
      <td>Riccardo Magliocchetti</td>
    </tr>
    <tr>
      <th>100</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>it</td>
      <td>HPC con Python: istruzioni per l'uso</td>
      <td>Nicola Creati</td>
    </tr>
    <tr>
      <th>101</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Resource Monitoring with Zabbix and Python</td>
      <td>Massimiliano Cuzzoli</td>
    </tr>
    <tr>
      <th>102</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Pytest &amp; Django are really good friends!!</td>
      <td>Simone Dalla</td>
    </tr>
    <tr>
      <th>103</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>django SHOP è ritornato</td>
      <td>Jacob Rief</td>
    </tr>
    <tr>
      <th>104</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>en</td>
      <td>djangoSHOP is back</td>
      <td>Jacob Rief</td>
    </tr>
    <tr>
      <th>105</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Django 💖Gulp</td>
      <td>Mattia Larentis</td>
    </tr>
    <tr>
      <th>106</th>
      <td>Talk</td>
      <td>Odoo</td>
      <td>it</td>
      <td>Odoo in Italia: La suite di applicazioni busin...</td>
      <td>Mario Riva</td>
    </tr>
    <tr>
      <th>107</th>
      <td>Talk</td>
      <td>Odoo</td>
      <td>it</td>
      <td>Primi passi in Odoo dev</td>
      <td>Eliumara Lopez</td>
    </tr>
    <tr>
      <th>108</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>jmb.mailup, uno strumento semplice per interfa...</td>
      <td>Benedetto Campanale</td>
    </tr>
    <tr>
      <th>109</th>
      <td>Talk</td>
      <td>Odoo</td>
      <td>it</td>
      <td>Sviluppare su Odoo</td>
      <td>Nicola Malcontenti</td>
    </tr>
    <tr>
      <th>110</th>
      <td>Talk</td>
      <td>Odoo</td>
      <td>it</td>
      <td>OCA, la community internazionale di Odoo: Come...</td>
      <td>Alex Comba</td>
    </tr>
    <tr>
      <th>111</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Perl6 is here to rest!</td>
      <td>David Mugnai</td>
    </tr>
    <tr>
      <th>112</th>
      <td>Talk</td>
      <td>Odoo</td>
      <td>it</td>
      <td>Gestione di un Consorzio con Odoo</td>
      <td>Piero Cecchi</td>
    </tr>
  </tbody>
</table>
<p>112 rows × 5 columns</p>
</div>



# Trainings


```python
rankings[rankings['type'].values == 'Training']
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>type</th>
      <th>track</th>
      <th>lang</th>
      <th>title</th>
      <th>speaker</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>Training</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Beautiful async code in Python 3</td>
      <td>Anton Caceres</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Training</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Docker: dalla build a production</td>
      <td>Davide Setti</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Training</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Computer Graphics per aspiranti game-developer...</td>
      <td>Roberto De Ioris</td>
    </tr>
    <tr>
      <th>38</th>
      <td>Training</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Python for System Administrators</td>
      <td>Roberto Polli</td>
    </tr>
    <tr>
      <th>56</th>
      <td>Training</td>
      <td>DjangoVillage</td>
      <td>en</td>
      <td>Scale and distribute your django backend app</td>
      <td>Marco Paolini</td>
    </tr>
    <tr>
      <th>60</th>
      <td>Training</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Master class for aiohttp usage</td>
      <td>Andrew Svetlov</td>
    </tr>
    <tr>
      <th>72</th>
      <td>Training</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Dive into object-oriented Python</td>
      <td>Leonardo Giordani</td>
    </tr>
    <tr>
      <th>75</th>
      <td>Training</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Genropy For Dummies</td>
      <td>Francesco Porcari</td>
    </tr>
    <tr>
      <th>89</th>
      <td>Training</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Dive into object-oriented Python</td>
      <td>Leonardo Giordani</td>
    </tr>
    <tr>
      <th>98</th>
      <td>Training</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Rendi scalabile la tua app django</td>
      <td>Marco Paolini</td>
    </tr>
  </tbody>
</table>
</div>



# Talks


```python
talks = rankings[rankings['type'].values == 'Talk']
```

## Main Conference Track: (*aka Python & Friends*)


```python
main_conf_talks = talks[talks['track'].values == 'Python & Friends']
main_conf_talks
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>type</th>
      <th>track</th>
      <th>lang</th>
      <th>title</th>
      <th>speaker</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Gestione di errori ed eccezioni in Python 2 e ...</td>
      <td>Alex Martelli</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Domotica a cinque euro con Raspberry Pi Zero e...</td>
      <td>Anna Chiara Bellini</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Exception and error handling in Python 2 and P...</td>
      <td>Alex Martelli</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Capire i Decoratori</td>
      <td>Ezio Melotti</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Ripensare la programmazione: un approccio funz...</td>
      <td>Francesco Bruni</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Delivery isn't magic anymore: distribuisci le ...</td>
      <td>Alan Franzoni</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Mischiare threads e fork sotto unix: cose da f...</td>
      <td>Enrico Franchi</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Big data con PostgreSQL</td>
      <td>Giuseppe Broccolo</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Continuous delivery of a Python web project wi...</td>
      <td>Joost Cassee</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>$5 Home Automation with Raspberry Pi Zero and ...</td>
      <td>Anna Chiara Bellini</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>EuroCotoletta 2017</td>
      <td>Christian Barra</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Mixing multiprocessing and threads in the UNIX...</td>
      <td>Enrico Franchi</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Introduction of aiohttp</td>
      <td>Andrew Svetlov</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Understanding Decorators</td>
      <td>Ezio Melotti</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Building an asynchronous websocket server</td>
      <td>Tatiana Al-Chueyr</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>La vita di uno sviluppatore di free software</td>
      <td>Riccardo Magliocchetti</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Abstract Base Classes: un uso intelligente del...</td>
      <td>Leonardo Giordani</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Strings don't exist</td>
      <td>Martin Matusiak</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Tox as project descriptor: not only Continuous...</td>
      <td>Roberto Polli</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Ansible: automazione IT vocata al Cloud</td>
      <td>Ivan Rossi</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Comando di un robot con Python</td>
      <td>Antonio Spadaro</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Pglogical: il futuro della replica con Postgres</td>
      <td>Marco Nenciarini</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>How to fight with yourself and win</td>
      <td>Christian Barra</td>
    </tr>
    <tr>
      <th>34</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>PyContinuous Integration: una esperienza di vita</td>
      <td>Giulio Calacoci</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Introduzione a MicroPython e BBC Micro:Bit</td>
      <td>Andrea Grandi</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>DukPy, liberarsi dalle catene di NodeJS</td>
      <td>Alessandro Molina</td>
    </tr>
    <tr>
      <th>40</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>CONNEXION: API FIRST REST FRAMEWORK FOR PYTHON</td>
      <td>João Santos</td>
    </tr>
    <tr>
      <th>41</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Abstract Base Classes: a smart use of metaclasses</td>
      <td>Leonardo Giordani</td>
    </tr>
    <tr>
      <th>42</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Introduction to MicroPython and BBC micro:bit</td>
      <td>Andrea Grandi</td>
    </tr>
    <tr>
      <th>46</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Introduction to JSON Schema</td>
      <td>Julian Berman</td>
    </tr>
    <tr>
      <th>48</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Iottly, open source Internet of Things distrib...</td>
      <td>Stefano Terna</td>
    </tr>
    <tr>
      <th>49</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Fixing memory leaks with tracemalloc and gc</td>
      <td>Marco Paolini</td>
    </tr>
    <tr>
      <th>51</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Multicorn: unicorni e elefanti possono lavorar...</td>
      <td>Giulio Calacoci</td>
    </tr>
    <tr>
      <th>52</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>A huge green snake bars the way!; Or, and Exer...</td>
      <td>Katie Silverio</td>
    </tr>
    <tr>
      <th>54</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Sistemare i memory leaks con tracemalloc e gc</td>
      <td>Marco Paolini</td>
    </tr>
    <tr>
      <th>57</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Docker e PostgreSQL: un matrimonio possibile?</td>
      <td>Leonardo Cecchi</td>
    </tr>
    <tr>
      <th>59</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Introduzione a "Modern OpenGL" con Python</td>
      <td>Roberto De Ioris</td>
    </tr>
    <tr>
      <th>61</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Java VS Python</td>
      <td>Simone Federici</td>
    </tr>
    <tr>
      <th>62</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Erpy: una solida base per scrivere gestionali ...</td>
      <td>Giovanni Porcari</td>
    </tr>
    <tr>
      <th>63</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Genropy: non solo gestionali</td>
      <td>Francesco Porcari</td>
    </tr>
    <tr>
      <th>64</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Taking care of PostgreSQL with Ansible</td>
      <td>Rubens Souza</td>
    </tr>
    <tr>
      <th>71</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Un CRM con Genropy,e altro</td>
      <td>Alessandro Tufi</td>
    </tr>
    <tr>
      <th>77</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Iottly, distribuzione open source per Internet...</td>
      <td>Stefano Terna</td>
    </tr>
    <tr>
      <th>78</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Auditing di un database PostgreSQL con Psycopg...</td>
      <td>Marco Nenciarini</td>
    </tr>
    <tr>
      <th>79</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Convalida dei dati per esseri umani</td>
      <td>Nicola Iarocci</td>
    </tr>
    <tr>
      <th>80</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Una storia di mille storie, con due punti ferm...</td>
      <td>carloratm carloratm</td>
    </tr>
    <tr>
      <th>84</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Autocompletamento per Blender Game Engine logic</td>
      <td>Anna Chiara Bellini</td>
    </tr>
    <tr>
      <th>86</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Python come Hardware Description Language</td>
      <td>Paolo Guadagnuolo</td>
    </tr>
    <tr>
      <th>88</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Fate RPG: una web application per giocarlo onl...</td>
      <td>Saverio Porcari</td>
    </tr>
    <tr>
      <th>90</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>From Java to Python</td>
      <td>OFFER SHARABI</td>
    </tr>
    <tr>
      <th>91</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Monitoraggio delle Risorse con Zabbix e Python</td>
      <td>Massimiliano Cuzzoli</td>
    </tr>
    <tr>
      <th>96</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Come passare indenni (o quasi) la traversata d...</td>
      <td>Ugo Scaiella</td>
    </tr>
    <tr>
      <th>97</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Blender Game Engine logic and autocompletion</td>
      <td>Anna Chiara Bellini</td>
    </tr>
    <tr>
      <th>101</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>en</td>
      <td>Resource Monitoring with Zabbix and Python</td>
      <td>Massimiliano Cuzzoli</td>
    </tr>
    <tr>
      <th>108</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>jmb.mailup, uno strumento semplice per interfa...</td>
      <td>Benedetto Campanale</td>
    </tr>
    <tr>
      <th>111</th>
      <td>Talk</td>
      <td>Python &amp; Friends</td>
      <td>it</td>
      <td>Perl6 is here to rest!</td>
      <td>David Mugnai</td>
    </tr>
  </tbody>
</table>
</div>




```python
print('Number of Talks Proposed: ', main_conf_talks['type'].count())
```

    Number of Talks Proposed:  56


# Sub Communities

<div style="background-color: #FAFAFA">
    <img src='https://raw.githubusercontent.com/leriomaggio/pycon7-community-voting/master/logos/djangovillage.png' style="align: center;" />
</div>


```python
djangovillagers = talks[talks['track'].values == 'DjangoVillage']
djangovillagers
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>type</th>
      <th>track</th>
      <th>lang</th>
      <th>title</th>
      <th>speaker</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>12</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>en</td>
      <td>Dockerizing Django projects</td>
      <td>Roberto Rosario</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>en</td>
      <td>What we understood about Microservices</td>
      <td>Saverio Mucci</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Grafici interattivi con Django e Highcharts JS...</td>
      <td>ERNESTO ARBITRIO</td>
    </tr>
    <tr>
      <th>43</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Django e i test: alcuni supporti per vivere fe...</td>
      <td>Iacopo Spalletti</td>
    </tr>
    <tr>
      <th>47</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>en</td>
      <td>Django tasty salad: DOs and DON'Ts using Celery</td>
      <td>Roberto Rosario</td>
    </tr>
    <tr>
      <th>58</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Debito tecnico: come non andare in rosso</td>
      <td>Simone Basso</td>
    </tr>
    <tr>
      <th>65</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Elasticsearch Blueprint</td>
      <td>Christian Strappazzon</td>
    </tr>
    <tr>
      <th>66</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Django e i metadati</td>
      <td>Iacopo Spalletti</td>
    </tr>
    <tr>
      <th>68</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Come integrare elasticsearch e dormire sonni t...</td>
      <td>Martino Pizzol</td>
    </tr>
    <tr>
      <th>69</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Progetti a prezzo fisso e l'Agile</td>
      <td>Peter Bittner</td>
    </tr>
    <tr>
      <th>73</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>en</td>
      <td>Developing a developer-friendly hypermedia API...</td>
      <td>Joost Cassee</td>
    </tr>
    <tr>
      <th>76</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>en</td>
      <td>Fix-Price Projects And Agile</td>
      <td>Peter Bittner</td>
    </tr>
    <tr>
      <th>87</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Progetti acceptance test-driven con Django</td>
      <td>Peter Bittner</td>
    </tr>
    <tr>
      <th>92</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Django e frontend? Gulp! Razionalizzare la ges...</td>
      <td>Alberto Motta</td>
    </tr>
    <tr>
      <th>95</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>en</td>
      <td>Acceptance Test-driven Projects With Django</td>
      <td>Peter Bittner</td>
    </tr>
    <tr>
      <th>99</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Viaggiare leggeri col proprio progetto Django</td>
      <td>Riccardo Magliocchetti</td>
    </tr>
    <tr>
      <th>102</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Pytest &amp; Django are really good friends!!</td>
      <td>Simone Dalla</td>
    </tr>
    <tr>
      <th>103</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>django SHOP è ritornato</td>
      <td>Jacob Rief</td>
    </tr>
    <tr>
      <th>104</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>en</td>
      <td>djangoSHOP is back</td>
      <td>Jacob Rief</td>
    </tr>
    <tr>
      <th>105</th>
      <td>Talk</td>
      <td>DjangoVillage</td>
      <td>it</td>
      <td>Django 💖Gulp</td>
      <td>Mattia Larentis</td>
    </tr>
  </tbody>
</table>
</div>




```python
print('Number of Talks Proposed: ', djangovillagers['type'].count())
```

    Number of Talks Proposed:  20


<div style="background-color: #FAFAFA">
    <img src='https://raw.githubusercontent.com/leriomaggio/pycon7-community-voting/master/logos/pydata.png' style="align: center;" />
</div>


```python
pydataers = talks[talks['track'].values == 'PyData']
pydataers
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>type</th>
      <th>track</th>
      <th>lang</th>
      <th>title</th>
      <th>speaker</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>9</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>it</td>
      <td>Reti Neurali in Python</td>
      <td>Simone Piunno</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>en</td>
      <td>Time Travel and Time Series Analysis with pand...</td>
      <td>Alexander Hendorf</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>en</td>
      <td>Building Data Pipelines in Python</td>
      <td>Marco Bonzanini</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>en</td>
      <td>%%async_run: an IPython notebook magic for asy...</td>
      <td>Valerio Maggio</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>en</td>
      <td>Pythonic Particles</td>
      <td>Valerio Maggio</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>en</td>
      <td>Machine learning and IoT for automatic presenc...</td>
      <td>Stefano Terna</td>
    </tr>
    <tr>
      <th>44</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>en</td>
      <td>How to deploy scikit-learn machine learning mo...</td>
      <td>Alex Casalboni</td>
    </tr>
    <tr>
      <th>45</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>en</td>
      <td>Contagious Functional Concepts in Python and t...</td>
      <td>Holger Peters</td>
    </tr>
    <tr>
      <th>50</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>en</td>
      <td>Cython extends Python</td>
      <td>Stefan Behnel</td>
    </tr>
    <tr>
      <th>53</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>it</td>
      <td>Metodi e  Strumenti per il Model Based Testing</td>
      <td>Aniello Barletta</td>
    </tr>
    <tr>
      <th>55</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>en</td>
      <td>Data Mangling with mongoDB the Right Way</td>
      <td>Alexander Hendorf</td>
    </tr>
    <tr>
      <th>67</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>it</td>
      <td>Machine learning e IoT per la rilevazione auto...</td>
      <td>Stefano Terna</td>
    </tr>
    <tr>
      <th>70</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>en</td>
      <td>Automatic English text correction</td>
      <td>Tatiana Al-Chueyr</td>
    </tr>
    <tr>
      <th>74</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>it</td>
      <td>Applied Bayesian Inference with PyMC</td>
      <td>Marco Santoni</td>
    </tr>
    <tr>
      <th>81</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>en</td>
      <td>Devops lessons for the data scientist</td>
      <td>Luca Mearelli</td>
    </tr>
    <tr>
      <th>82</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>it</td>
      <td>Automatizzare la creazione e gestione di un cl...</td>
      <td>Paolo D'Onorio De Meo</td>
    </tr>
    <tr>
      <th>83</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>it</td>
      <td>Aiuto !!! Ho un dataset "squilibrato" !</td>
      <td>Christian Barra</td>
    </tr>
    <tr>
      <th>85</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>it</td>
      <td>Introduzione a Orange Data Mining</td>
      <td>Eric Bonfadini</td>
    </tr>
    <tr>
      <th>93</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>it</td>
      <td>In-Database analytics with python and monetdb</td>
      <td>Danilo Maurizio</td>
    </tr>
    <tr>
      <th>94</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>it</td>
      <td>Lezioni devops per data scientist</td>
      <td>Luca Mearelli</td>
    </tr>
    <tr>
      <th>100</th>
      <td>Talk</td>
      <td>PyData</td>
      <td>it</td>
      <td>HPC con Python: istruzioni per l'uso</td>
      <td>Nicola Creati</td>
    </tr>
  </tbody>
</table>
</div>




```python
print('Number of Talks Proposed: ', pydataers['type'].count())
```

    Number of Talks Proposed:  21


<div style="background-color: #FAFAFA">
    <img src='https://raw.githubusercontent.com/leriomaggio/pycon7-community-voting/master/logos/odoo.png' style="align: center;" />
</div>


```python
odooers = talks[talks['track'].values == 'Odoo']
odooers
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>type</th>
      <th>track</th>
      <th>lang</th>
      <th>title</th>
      <th>speaker</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>106</th>
      <td>Talk</td>
      <td>Odoo</td>
      <td>it</td>
      <td>Odoo in Italia: La suite di applicazioni busin...</td>
      <td>Mario Riva</td>
    </tr>
    <tr>
      <th>107</th>
      <td>Talk</td>
      <td>Odoo</td>
      <td>it</td>
      <td>Primi passi in Odoo dev</td>
      <td>Eliumara Lopez</td>
    </tr>
    <tr>
      <th>109</th>
      <td>Talk</td>
      <td>Odoo</td>
      <td>it</td>
      <td>Sviluppare su Odoo</td>
      <td>Nicola Malcontenti</td>
    </tr>
    <tr>
      <th>110</th>
      <td>Talk</td>
      <td>Odoo</td>
      <td>it</td>
      <td>OCA, la community internazionale di Odoo: Come...</td>
      <td>Alex Comba</td>
    </tr>
    <tr>
      <th>112</th>
      <td>Talk</td>
      <td>Odoo</td>
      <td>it</td>
      <td>Gestione di un Consorzio con Odoo</td>
      <td>Piero Cecchi</td>
    </tr>
  </tbody>
</table>
</div>




```python
print('Number of Talks Proposed: ', odooers['type'].count())
```

    Number of Talks Proposed:  5

