users.updateMasksV2

$description
Производит битовые операции над масками указанных пользователей и и сохраняет результат. Если параметр маски для операции не указаны, то возвращает текущее значение масок указанных пользователей.

$params#uids
Список разделенных запятыми идентификаторов пользователей. Макс. число идентификаторов составляет 100.

$params#or_mask
Маска которая будет добавлена (OR) к текущей маске

$params#and_mask
Маска, которая будет умножена (AND) с текущей маской

$additional
Маска пользователя – это 32 бит информации для каждого пользователя, специфичной для вызывающего приложения. Приложение может считывать, устанавливать и производить логические операции над битами маски.
Маска пользователя используется для битовой фильтрации в {% replace_method notifications.sendMass %} нотификациях, а также может использоваться для хранения любой другой информации.

* Метод всегда возвращает результирующее значение маски пользователя в десятичной системе счисления.
* Никто, кроме приложения не имеет возможности менять маску пользователя.
* Операции над маской возможны даже для тех пользователей, которые со временем удалили приложение.