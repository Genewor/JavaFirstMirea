# DoctorFriend
## Описание проекта
Приложение создано для удобного взаимодействия между
пациентами и врачами.

__UPD__: часть фич (скорее всего все, кроме фич, связанных с главным экраном) будут оставлены до лучших времен.

Для пациентов приложение позволяет:
- зайти в свой личный кабинет и отредактировать поменявшиеся данные
- посмотреть историю посещения врачей, результаты их посещения
- посмотреть результаты анализов
- записаться к врачам различных специальностей по доступному времени

Для врачей приложение позволяет:
- зайти в свой личный кабинет и отредактировать поменявшиеся данные
- посмотреть записи к себе на текущий день/неделю/месяц
- посмотреть информацию о пациентах, которые к тебе записаны
- поставить диагноз и провести исследование, внеся изменения в карту пациента
## Логика работы приложения
Пользователи бывают двух типов: пациенты и врачи. Каждому из них
предоставляется свой функционал. Есть изначальный экран, на котором
показываются либо записи к врачам, либо записи пациентов к врачу.
При клике на запись можно увидеть детали записи или пациента,
записанного к врачу.

Также можно зайти в свой личный кабинет (через меню)
и посмотреть информацию о пользователе (отдельная кнопка для возможности
изменить данную информацию).

При активном сеансе посещения доктора пациентами, врач может вносить изменения
в лист пациента и, при окончании встречи, данные заносятся в карту пациента.
Также врач может заносить результаты анализов пациента в его карту.

Врач может посмотреть будущих пациентов, которые к нему записаны.
Пациент может посмотреть историю посещения врачей и результаты своих анализов.

(Для каждой из вышеперечисленных фич свой экран).
## Стек используемых технологий
Java (17 version), Swing. Архитектура проекта будет построена по MVC.
## Примерный UML проекта (которого нету =) )
User <- Doctor & Patient; Screen, MainScreen, AppointmentDetailsScreen,
PatientDetailsScreen, AppointmentHistoryScreen, MakeAppointmentScreen,
UserSettingsScreen, AddAnalysisToPatientScreen, CurrentAppointmentScreen,
FutureAppointmentsScreen (both for doctor and patient?),
AnalysisResultsScreen; UserDatabase (Singleton), UserRepository?,
AppointmentFactory; "Some interfaces to implement similar logic";
