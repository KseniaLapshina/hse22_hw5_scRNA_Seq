# hse22_hw5

https://colab.research.google.com/drive/1bs0h8NfNTSsvFczVYo_5B_ylcNUf1vhf?usp=sharing

## Метод нормализации данных.
Сравнение "сырых" данных с высокой вероятностью даст некорректный результат, так как разница в экспресси может быть обусловлена не дифференциальной экспрессией генов, а в целом разным уровнем экспрессии клетками(т.е. общий уровень экспрессии меняется, а соотношения экспрессий генов - нет). Для компенсации этого эффекта используется RPM(reads per million), число чтений для гена делят на общее число чтений для образца и умножают на миллион.

Также при нормализации учитывают тот факт, что при одинаковом уровне экспрессии на длинные гены приходится больше чтений, чем на короткие. Чтобы компенсировать этот эффект используют RPK(reads per kilobase), число чтений для гена делят на длину гена и умножают на тысячу.

Идеальным можно считать использование методов TPM(transcript per million) и RPKM (reads per kilobase per million), они сочетают в себе номализацию на общий уровень экспрессии и нормализацию на длину.

Однако применение RPK, а значит и TPM, и RPKM в нашей работе невозможно, так как у нас отсутствуют данные по длинам генов, соответственно, мы применяем метод RPM.

## Heatmap для экспрессии маркерных генов.
![image](https://user-images.githubusercontent.com/114621114/206863350-45359804-65f1-4403-9261-82f5a626c8d8.png)

## Полученные визуализации UMAP и PCA.
![image](https://user-images.githubusercontent.com/114621114/206863390-343ae7e7-2367-4b46-9114-78a1d0af78eb.png)
![image](https://user-images.githubusercontent.com/114621114/206863398-3cf8d023-e318-4002-a699-65547ccf8319.png)

## Анализ результатов
PCA плохо справляется в выделением кластеров, UMAP лучше справляется с этой задачей. PCA лучше всего отделяет кластер mTEC-I, UMAP - MTEC-IV.
