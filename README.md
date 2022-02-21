# hse_hw1_meth
### Ссылка на колаб
https://colab.research.google.com/drive/1PEeIDy3hm5tl3l2QtsxmULoJSB_BCMTw?usp=sharing

## Анализ QC прочтений
![Снимок экрана от 2022-02-21 21-09-28](https://user-images.githubusercontent.com/93282657/155007656-7d1113eb-7e99-4a71-b238-aed15f160fea.png) ![Снимок экрана от 2022-02-21 21-09-17](https://user-images.githubusercontent.com/93282657/155007665-a528711b-ea7a-4910-be61-be3d1be25c66.png)




## Таблица (пункты a и b)
Образец | 11347700-11367700 | 40185800-40195800 | Deduplicated % |  
 --- |--- |--- |--- 
Cell 8 | 1090 | 464 | 81.69 | 
ICM | 1456 | 630 | 90.92 | 
Epiblast | 2328 | 1062 | 97.08 | 

## M-bias plot
ICM | Epiblast | Cell 8 |
 --- |--- |--- 
![Снимок экрана от 2022-02-21 21-23-46](https://user-images.githubusercontent.com/93282657/155009257-e4cb0484-67fc-405b-ac2d-b9123d9fab6e.png) |![Снимок экрана от 2022-02-21 21-26-36](https://user-images.githubusercontent.com/93282657/155009589-e1bf0802-a3a9-49a7-ad32-17c9e126dcf7.png) |![Снимок экрана от 2022-02-21 21-30-00](https://user-images.githubusercontent.com/93282657/155010004-fefe226b-be8f-4a75-a227-2a97218ef335.png) |


## Гистограмма с общим уровнем метилирования для каждого из образца
Код построения одного из графиков:

    df_icm = pd.read_csv("s_epiblast.deduplicated.bedGraph", delimiter = '\t', header = None, skiprows = 1)
    plt.figure(figsize = (8, 5))
    plt.hist(df_icm[3], bins = 70, density = True)
    plt.title("Распределение метилирования icm")
    plt.xlabel("Процент метилированных цитозинов")
    plt.ylabel("Частота")
    plt.show()


![Снимок экрана от 2022-02-21 14-02-14](https://user-images.githubusercontent.com/93282657/155008635-383fd965-600c-4bef-97c3-250e7557ff0c.png)
![Снимок экрана от 2022-02-21 14-02-04](https://user-images.githubusercontent.com/93282657/155008637-86c250c2-697f-4ca3-b6ad-55f39dd64060.png)
![Снимок экрана от 2022-02-21 14-01-53](https://user-images.githubusercontent.com/93282657/155008640-ceb056d5-9c0e-41d2-8de0-75b5b962517b.png)




