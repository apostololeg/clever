Использование QGroundControl через Wi-Fi
===

Возможен контроль, управление и настройка полетного контроллера квадрокоптера с помощью программы QGroundControl по Wi-Fi. Для этого необходимо подключиться к Wi-Fi сети `CLEVER-xxxx`.

TCP-бридж
---

Необходимо убедиться с в launch-файле Клевера (`~/catkin_ws/src/clever/clever/launch/clever.launch`) включен TCP GCS Bridge:

```xml
<arg name="gcs_bridge" default="tcp"/>
```

При изменени launch-файла необходимо перезагрузить сервис `clever`:

```bash
sudo systemctl restart clever
```

Затем в программе QGroundControl нужно выбрать Application Settings -> Comm Links -> Add. Создать подключение со следующими настройками:

![](/assets/bridge_tcp.png)

Затем необходимо выбрать в списке подключений "Clever" и нажать "Connect". После этого можно будет настраивать, калибровать и просматривать состояние квадкоптера без проводов:

![](/assets/qground.png)

UDP-бридж
---

TODO
