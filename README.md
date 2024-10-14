# Project_Sprint_5_Vehicles
Link do projeto(Render): https://project-sprint-5-vehicles.onrender.com


Rafael, 
Não localizei o problema de idennção no app.py no primeiro IF e quais mais alterações a realizar. O que mais precisa ser feito por favor?










Rafa, será por conta dos amibientes abaixo? Para mim não aparece erro. Rodaram os gráficos normalmente. Abaixo veja os ambientes e demais prints. No appy aparece erro no output. Pode me ajudar a identificar onde estao os erros? Grata.

(base) C:\Users\Samsung>conda env list
# conda environments:
#
base                  *  C:\Users\Samsung\_anaconda
sprint5                  C:\Users\Samsung\_anaconda\envs\sprint5
vehicle_env              C:\Users\Samsung\_anaconda\envs\vehicle_env
                         C:\Users\Samsung\anaconda3
vehicle_env              c:\Users\Samsung\_anaconda\envs\vehicle_env


Os arquivos readm.me e gitignore estão dentro do Project_Sprint_5_Vehicles. Não sei se isso pode ser um problema, ou seja, os arquivos não estão diretamente dentro da Sprint_5.

(base) C:\Users\Samsung\Sprint_5>dir
 O volume na unidade C não tem nome.
 O Número de Série do Volume é 78A4-27A5

 Pasta de C:\Users\Samsung\Sprint_5

09/10/2024  22:48    <DIR>          .
09/10/2024  22:48    <DIR>          ..
10/10/2024  00:25    <DIR>          Project_Sprint_5_Vehicles
               0 arquivo(s)              0 bytes
               3 pasta(s)   88.574.447.616 bytes disponíveis


  No app.py: 
  import pandas as pd
import plotly.express as px
import streamlit as st

car_data = pd.read_csv('vehicles_us.csv') # lendo os dados
hist_button = st.button('Criar histograma') # criar um botão

if hist_button: # se o botão for clicado
    # escrever uma mensagem
    st.write('Criando um histograma para o conjunto de dados de anúncios de vendas de carros')
    
    # criar um histograma
    fig = px.histogram(car_data, x="odometer")

    # exibir um gráfico Plotly interativo
    st.plotly_chart(fig, use_container_width=True)        

disp_button = st.button('Criar gráfico de dispersão') # criar um botão
if disp_button: # se o botão for clicado
    # escrever uma mensagem
    st.write('Criando um gráfico de dispersão para o conjunto de dados de anúncios de vendas de carros')

    # criar um histograma
    fig = px.scatter(car_data, x="odometer", y="price")

    # exibir um gráfico Plotly interativo
    st.plotly_chart(fig, use_container_width=True)


  PROBLEMS
   Em app.py apareceu mensagens de erro na importação das bibliotecas pandas, plotly e streamlit, então instalei novamente pelo terminal.
 Import "pandas" could not be resolved [Ln 3, Col 8]
 Import "plotly.express" could not be resolved [Ln 3, Col 8]
 Import "streamlit" could not be resolved [Ln 3, Col 8]

 
 No Source Control (Staged Changes) ele fica rodando o Commit e não para. Parece não estar atualizando o Git. Apesar que chequei no terminal com git push e a mensagem foi:  C:\Users\Samsung\Sprint_5\Project_Sprint_5_Vehicles> git push
Everything up-to-date

C:\Users\Samsung\Sprint_5\Project_Sprint_5_Vehicles\README.md [472ms]
2024-10-14 13:33:28.685 [info] > git log --format=%H%n%aN%n%aE%n%at%n%ct%n%P%n%D%n%B -z --shortstat --diff-merges=first-parent -n50 --skip=0 --topo-order --decorate=full --stdin [950ms]
 
 Em # Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# On branch main
# Your branch is up to date with 'origin/main'.
#
# Changes to be committed:
#	modified:   README.md
#	modified:   Streamlit/config.toml
#	modified:   app.py
