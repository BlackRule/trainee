# Тестовые задания на стажировку Frontend KODE

## 1. Преобразование данных

Требуется написать функцию, приводящую объект формата

```
type Input = {
  [projectId: string]: {
    [sceneId: string]: {
      title: string
      description: string
      value: number
    }
  }
}
```

в массив типа Output с элементами типа Item

```
type Item = {
  projectId: string
  sceneId: string
  value: number
}
type Output = Item[]
```

Результат должен содержать массив типов Item, в элементах которого значение value > 0

Пример входящего объекта:

```
const input = {
  p1: {
    s1: {
      title: 'scene 1',
      description: 'description 1',
      value: 1,
    },
    s2: {
      title: 'scene 2',
      description: 'description 2',
      value: 32,
    },
    s3: {
      title: 'scene 3',
      description: 'description 3',
      value: 89,
    },
    s4: {
      title: 'scene 3',
      description: 'description 3',
      value: 0,
    },
  },
  p2: {
    s5: {
      title: 'scene 5',
      description: 'description 5',
      value: 0,
    },
    s6: {
      title: 'scene 6',
      description: 'description 6',
      value: 42,
    },
    s7: {
      title: 'scene 7',
      description: 'description 7',
      value: -9,
    },
  },
}
```

Результат выполнения функции:

```
[
  { projectId: 'p1', sceneId: 's1', value: 1, title: 'scene 1' },
  { projectId: 'p1', sceneId: 's2', value: 32, title: 'scene 2' },
  { projectId: 'p1', sceneId: 's3', value: 89, title: 'scene 3' },
  { projectId: 'p2', sceneId: 's6', value: 42, title: 'scene 6' },
]
```

Дополнительное задание:
Добавить в функцию сортировку результата по полю value, от большего к меньшему.

## 2. Покемоны!

Требуется реализовать приложение Покемоны! используя следующий стэк:

- Create React App
- React
- Redux
- React-router

### Функциональность приложения:

Приложение использует публичное API - https://pokemontcg.io/ и содержит два экрана

- Экран 1 - Вывод списка доступных сетов (/sets)
  По клику на сет - переход на второй экран

  ![Экран 1](screen1.png?raw=true "Экран 1")

- Экран 2 - Вывод всех карт, принадлежащих выбранному сету (/cards?setCode={setCode})

  ![Экран 2](screen2.png?raw=true "Экран 2")

- Верстка проекта должна быть адаптивной и максимально приближенной к указанным изображениям. Использовать FlexBox layout.

Будет плюсом любая дополнительная функциональность приложения up to you (анимации, пагинация/бесконечный скролл, обработка ошибок и т.д.)

### Результат

Проект разместить на вашем github и указать в readme.md:

- Декомпозиция проекта. Оценить задачи, поставить предполагаемое время выполнения
- Описать с какими сложностями столкнулись и как их решили
- Дополнительная функциональность (если реализовано)
