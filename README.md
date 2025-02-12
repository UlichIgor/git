### ***Інструкція по роботі з Git***
 **Git** — це швидка розподілена система контролю версій.
* ```git init```— ініціалізує новий репозиторій **GIT** та починає відстеження існуючого каталогу. До існуючого каталогу додається прихована вкладена папка, в якій розміщується внутрішня структура даних, необхідна для керування версіями.
* ```git clone```— створює локальну копію проекту, який існує віддалено. Клон включає всі файли проекту, журнал і гілки.
* ```git add```- Готує зміну. **GIT** відстежує зміни в базі коду розробника, але для включення змін до журналу проекту необхідно готувати їх та створювати моментальні знімки. Ця команда виконує першу частину цього двоетапного процесу, тобто підготовку. Усі підготовлені зміни стануть частиною наступного моментального знімка та журналу проекту. Роздільна підготовка та фіксація дають розробникам повний контроль над історією проекту без необхідності змінювати підхід до написання коду та роботи в цілому.
* ```git commit``` — зберігає моментальний знімок у журналі проекту та завершує процес відстеження змін. Інакше висловлюючись, фіксація схожа створення фотографії. Все, що було підготовлено за допомогою команди ``git add``, стане частиною моментального знімка під час використання ``git commit``.
* ```git status``` - виводить стан змін: які не відстежуються, змінені чи підготовлені.
* ```git branch```- Показує гілки, з якими ведеться локальна робота.
* ```git merge```- Виконує злиття ліній розробки. Ця команда зазвичай застосовується для поєднання змін, внесених у двох різних гілках. Наприклад, розробник виконує злиття, коли необхідно поєднати зміни з гілки функції з головною гілкою для розгортання.
* ``` git pull```— застосовує до локальної лінії розробки оновлення віддалений аналог. Розробники використовують цю команду, якщо колега виконав фіксації у галузі віддаленого репозиторію і ці зміни потрібно відобразити в локальному середовищі.
* ```git push```- оновлює віддалений репозиторій з урахуванням фіксацій, виконаних у гілки локально.
