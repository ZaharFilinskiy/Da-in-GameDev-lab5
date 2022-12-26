# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #5 выполнил(а):
- Филинский Захар Евгеньевич
- РИ211121
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 80 |
| Задание 2 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.
- ✨Magic ✨

## Цель работы
Познакомиться с программными средствами реализации "глубокого обучения" и его интеграции в Unity.

## Задание 1
### Изменить параметры файла. yaml-агента и определить какие параметры и как влияют на обучение модели.

Установив все нужные структуры и компоненты в редакторе unity  я приступил к обучению агента:
![2022-12-26_01-41-49](https://user-images.githubusercontent.com/114186148/209544339-ace3fff0-f9b4-449c-8764-30456f340db7.png)

Далее через Anaconda promt проделал подготовку к обучению и приступил непосредственно к нему:
![2022-12-26_16-44-44](https://user-images.githubusercontent.com/114186148/209545436-e9141177-6663-480f-a315-1e476b197d45.png)

После получив графики в TensorBoard, попробовал изменить параметры Yaml файлов для провреки какие из них влияют на обучение модели.

![2022-12-26_16-52-33](https://user-images.githubusercontent.com/114186148/209546078-26c72d63-1248-466a-a953-61fabf3a3278.png)
![2022-12-26_16-52-13](https://user-images.githubusercontent.com/114186148/209546081-d9903e73-ddc5-40e0-a537-361cc53c437b.png)

Изменив параметр Bath_size, я понял что агенту понадобилось больше времени на обучение. Как выясилось данный параметр отвечает за количество "эпох" обучения. И изменив его меняется и время необоходимое для обучения.

Далее я решил поработать с параметром Max steps, который отечает за максимальное количество данных которые могут быть обработаны за одно обучение.
Повысив данный параметр я ускорил работу агента во время эпохи обучения и тем самым повлиял на обучение модели.

![2022-12-26_16-59-26](https://user-images.githubusercontent.com/114186148/209546818-5e8f1810-0425-47e3-8a07-9558583efd8f.png)
![2022-12-26_16-58-50](https://user-images.githubusercontent.com/114186148/209546819-a561029a-8b87-48ba-a901-31781ed88cc7.png)

Поизменяв ещё параметров я пришёл к выводу, что обучение модели зависит не от одного параметра а от их совокупности. И каждый так или иначе влияет на скорость, результативность и т.п параметры обучения. 

## Задание 2
### Опиcать результаты, выведенные в TensorBoard.
Выолнив обучение и напрямую запустив tensor board я увидел графики,которые помогают понять структуру и производительность обучения.
Графа Scalars показывает различные параметры от которых зависит обучение. К примеру Длительность обучения, количество наград, количество полученной валюты и т.п
![image](https://user-images.githubusercontent.com/114186148/209480641-81550095-9e7c-4ebc-893e-c5c6c5a194c0.png)

Гарфа Distributions показывает общее распределение. В нашем случае в виде фигур, как получение наград за всё обучение.
![2022-12-26_01-43-13](https://user-images.githubusercontent.com/114186148/209548625-75e4f259-5cac-4423-8d75-f6e8b16ce763.png)

Histograms и Text соттветсвенно выводят значения в виде гистограмм и текста.

Данные занчения и графики также изменялись при редактировании параметров yaml файла. Особенно данные связанные с наградами увеличивались при замене max steps и уменьшались при замене bath size.
## Выводы
Обучение модели непростое для понимания и редактирования занятие, оданко помогает это сделать и проанализировать веб-приложение - tensorboard, которое чертит всё в виде удобных глазу графиков, гистограмм и текстов. Различные конфигурации yaml файлов также показали, что обучение зависит от многих парметров в совокупности и в правильном их подборе кроется ключ к успеху. Ну и конечно я смог побольше интегрироваться в экономику игр в unity.
## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
