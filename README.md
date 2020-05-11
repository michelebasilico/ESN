# Data Visualization

dataVisualization.py: 
Permette la visualizzazione dei seguenti grafici:
1.  Timeseries(energia) dei device delle singole abitazioni
2.  Timeseries(potenza) dei device delle singole abitazioni
3.  Somma potenze consumate da tutti i device dello stesso tipo per ogni abitazione;
4.  Somma potenze consumate da tutti i device dello stesso tipo per tutto il vicinato;
5.  Potenze consumate dai singoli device per ogni abitazione;
6.  Potenze consumate dai singoli device per il vicinato;
7.  Autoconsumo, somma di potenze consumate e prodotte per ogni abitazione;
8.  Autoconsumo, somma di potenze consumate e prodotte per l'intero vicinato;
9.  Somma di potenze prodotte e consumate per ogni singola abitazione;
10. Somma di potenze prodotte e consumate per l'intero vicinato;
11. Torta Autoconsumo(energetico) ed energia rilasciata nella rete per ogni abitazione;
12. Torta Energia Prodotta ed Energia Consumata per ogni abitazione;
Lo script effettua la ricerca della cartella output all'interno della cartella di simulazione. In essa va poi a ricercare tutte le cartelle presenti. Ad ogni cartella è associato un dispositivo, il cui nome viene determinato dal nome della cartella stessa. All'interno di ogni cartella saranno presenti le timeserie dei device delle home dell'abtazione. L'id della home deve essere il primo carattere del nome del file. Questo verrà utilizzato per contraddistinguere le diverse home ed effettuare i calcoli per le singole home.



power.py: 
Libreria contente i moduli per la conversione Unix->Datatime e Energia->Potenza. Inoltre sono state aggiunte le seguenti funzioni
1. data_cleaning(df,date,start='',end'',freq'') -> Per la pulizia dei dati. In ingresso vuole il dataframe da pulire. Date invece è un valore booleano. Se True, indicare deve essere indicata la data sulla quale pulire il dataframe, oltre alla frequenza per ogni campione
2. dfEnergy_to_dfPower(df) -> Trasforma un dataframe con data e energia in un dataframe con data e potenza. Vuole unicamente il dataframe da convertire
3. sum_power(list_df) -> Somma le potenze di una lista di dataframe in base alla sequenza di date uguali. Vuole la lista di dataframe da sommare
4. diff_power(df1,df2) -> Differenza di potenze tra due dataframe. Viene sottratto df2 da df1
5. self_consumption(df_ProdTot,df_ConsTot ) -> Calcolo dell'autoconsumo. Vuole in ingresso un dataframe con la somma delle potenze dei produttori ed un altro con la somma delle potenze consumate
6.  plot_axis_dateFormatter -> Imposta il formato delle ascisse sul tipo data
