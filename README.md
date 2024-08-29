# Настройка ПК для создания стендов и выполнения домашних заданий
## Цель домашнего задания
    Настроить среду для выполнения домашних работ
## Описание домашнего задания
Подготовка ПК для выполнения домашних работ
    
В этом методическом указании рассмотрены основные инструкции по установке программ, которые понадобятся для выполнения домашних работ.
- Установка среды виртуализации VirtualBox.
- ПО для настройки виртуальной среды на базе VirtualBox и Hashicorp Vagrant.
- Среда автоматического конфигурирования — Ansible.
- Дополнительные программы, которые могут потребоваться для выполнения домашних работ.

# Настройка рабочего места в Debian/Ubuntu
>Работа выполнена на Ubuntu 22.04
1. Установка базовых программ для домашних заданий:

    a) Обновление списока пакетов:
    ```
    user@ws:~$ sudo apt update
    [sudo] пароль для user: 
    Сущ:1 https://repo.yandex.ru/yandex-browser/deb stable InRelease
    Сущ:2 http://ru.archive.ubuntu.com/ubuntu noble InRelease                                                   
    Пол:3 http://ru.archive.ubuntu.com/ubuntu noble-updates InRelease [126 kB]                                  
    Сущ:4 http://security.ubuntu.com/ubuntu noble-security InRelease                                                             
    Сущ:5 http://ru.archive.ubuntu.com/ubuntu noble-backports InRelease                                                          
    Сущ:6 https://packages.microsoft.com/repos/code stable InRelease                                                             
    Пол:7 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 Packages [463 kB]                                         
    Игн:8 https://apt.releases.hashicorp.com noble InRelease                                                                     
    Пол:9 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe amd64 Packages [337 kB]                                     
    Ошб:10 https://apt.releases.hashicorp.com noble Release                                                                      
      404  Not Found [IP: 3.164.230.117 443]
    Сущ:11 http://download.virtualbox.org/virtualbox/debian noble InRelease                                          
    Чтение списков пакетов… Готово            
    E: Репозиторий «https://apt.releases.hashicorp.com noble Release» больше не содержит файла Release.
    N: Обновление из этого репозитория нельзя выполнить безопасным способом, поэтому по умолчанию он отключён.
    N: Информацию о создании репозитория и настройках пользователя смотрите в справочной странице apt-secure(8).
    W: http://download.virtualbox.org/virtualbox/debian/dists/noble/InRelease: Ключ хранится в унаследованной связке ключей trusted.gpg (/etc/apt/trusted.gpg), подробности см. в разделе DEPRECATION в apt-key(8).

    ```

    b) Установка текстового редактора Vim:
    ```
    user@ws:~$ sudo apt install -y vim
    [sudo] пароль для user: 
    Попробуйте ещё раз.
    [sudo] пароль для user: 
    Чтение списков пакетов… Готово
    Построение дерева зависимостей… Готово
    Чтение информации о состоянии… Готово         
    Следующий пакет устанавливался автоматически и больше не требуется:
    ansible-core git-man hplip-data libdouble-conversion3 liberror-perl libgsoap-2.8.132t64 libhpmud0 libimagequant0 liblzf1
    libmd4c0 libpcre2-16-0 libqt5core5t64 libqt5dbus5t64 libqt5gui5t64 libqt5help5 libqt5network5t64 libqt5opengl5t64
    libqt5printsupport5t64 libqt5qml5 libqt5qmlmodels5 libqt5quick5 libqt5sql5-sqlite libqt5sql5t64 libqt5svg5
    libqt5waylandclient5 libqt5waylandcompositor5 libqt5widgets5t64 libqt5x11extras5 libqt5xml5t64 libraqm0 libsane-hpaio
    libsdl-ttf2.0-0 libsdl1.2debian libtpms0 libvncserver1 libxcb-xinerama0 libxcb-xinput0 printer-driver-hpcups
    printer-driver-postscript-hp python3-argcomplete python3-dnspython python3-jmespath python3-kerberos python3-libcloud
    python3-lockfile python3-ntlm-auth python3-olefile python3-packaging python3-passlib python3-pexpect python3-pil
    python3-ptyprocess python3-requests-ntlm python3-resolvelib python3-selinux python3-simplejson python3-winrm
    python3-xmltodict qt5-gtk-platformtheme qttranslations5-l10n qtwayland5
    Для его удаления используйте «sudo apt autoremove».
    Предлагаемые пакеты:
    ctags vim-doc vim-scripts
    Следующие НОВЫЕ пакеты будут установлены:
    vim
    Обновлено 0 пакетов, установлено 1 новых пакетов, для удаления отмечено 0 пакетов, и 150 пакетов не обновлено.
    Необходимо скачать 1 881 kB архивов.
    После данной операции объём занятого дискового пространства возрастёт на 4 229 kB.
    Пол:1 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 vim amd64 2:9.1.0016-1ubuntu7.1 [1 881 kB]
    Получено 1 881 kB за 3с (546 kB/s)   
    Выбор ранее не выбранного пакета vim.
    (Чтение базы данных … на данный момент установлен 198291 файл и каталог.)
    Подготовка к распаковке …/vim_2%3a9.1.0016-1ubuntu7.1_amd64.deb …
    Распаковывается vim (2:9.1.0016-1ubuntu7.1) …
    Настраивается пакет vim (2:9.1.0016-1ubuntu7.1) …
    update-alternatives: используется /usr/bin/vim.basic для предоставления /usr/bin/ex (ex) в автоматическом режиме
    update-alternatives: используется /usr/bin/vim.basic для предоставления /usr/bin/rview (rview) в автоматическом режиме
    update-alternatives: используется /usr/bin/vim.basic для предоставления /usr/bin/rvim (rvim) в автоматическом режиме
    update-alternatives: используется /usr/bin/vim.basic для предоставления /usr/bin/vi (vi) в автоматическом режиме
    update-alternatives: используется /usr/bin/vim.basic для предоставления /usr/bin/view (view) в автоматическом режиме
    update-alternatives: используется /usr/bin/vim.basic для предоставления /usr/bin/vim (vim) в автоматическом режиме
    update-alternatives: используется /usr/bin/vim.basic для предоставления /usr/bin/vimdiff (vimdiff) в автоматическом режиме 
    ```

    c) Установка программ для анализа сетевого трафика:        
    ```
    user@ws:~$ sudo apt install -y traceroute net-tools tcpdump 
    Чтение списков пакетов… Готово
    Построение дерева зависимостей… Готово
    Чтение информации о состоянии… Готово         
    Следующий пакет устанавливался автоматически и больше не требуется:
    ansible-core git-man hplip-data libdouble-conversion3 liberror-perl libgsoap-2.8.132t64 libhpmud0 libimagequant0 liblzf1
    libmd4c0 libpcre2-16-0 libqt5core5t64 libqt5dbus5t64 libqt5gui5t64 libqt5help5 libqt5network5t64 libqt5opengl5t64
    libqt5printsupport5t64 libqt5qml5 libqt5qmlmodels5 libqt5quick5 libqt5sql5-sqlite libqt5sql5t64 libqt5svg5
    libqt5waylandclient5 libqt5waylandcompositor5 libqt5widgets5t64 libqt5x11extras5 libqt5xml5t64 libraqm0 libsane-hpaio
    libsdl-ttf2.0-0 libsdl1.2debian libtpms0 libvncserver1 libxcb-xinerama0 libxcb-xinput0 printer-driver-hpcups
    printer-driver-postscript-hp python3-argcomplete python3-dnspython python3-jmespath python3-kerberos python3-libcloud
    python3-lockfile python3-ntlm-auth python3-olefile python3-packaging python3-passlib python3-pexpect python3-pil
    python3-ptyprocess python3-requests-ntlm python3-resolvelib python3-selinux python3-simplejson python3-winrm
    python3-xmltodict qt5-gtk-platformtheme qttranslations5-l10n qtwayland5
    Для его удаления используйте «sudo apt autoremove».
    Следующие НОВЫЕ пакеты будут установлены:
    net-tools tcpdump traceroute
    Обновлено 0 пакетов, установлено 3 новых пакетов, для удаления отмечено 0 пакетов, и 150 пакетов не обновлено.
    Необходимо скачать 743 kB архивов.
    После данной операции объём занятого дискового пространства возрастёт на 2 317 kB.
    Пол:1 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 tcpdump amd64 4.99.4-3ubuntu4 [479 kB]
    Пол:2 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 net-tools amd64 2.10-0.1ubuntu4 [204 kB]
    Пол:3 http://ru.archive.ubuntu.com/ubuntu noble/universe amd64 traceroute amd64 1:2.1.5-1 [60,5 kB]
    Получено 743 kB за 4с (208 kB/s)           
    Выбор ранее не выбранного пакета tcpdump.
    (Чтение базы данных … на данный момент установлено 198299 файлов и каталогов.)
    Подготовка к распаковке …/tcpdump_4.99.4-3ubuntu4_amd64.deb …
    Распаковывается tcpdump (4.99.4-3ubuntu4) …
    Выбор ранее не выбранного пакета net-tools.
    Подготовка к распаковке …/net-tools_2.10-0.1ubuntu4_amd64.deb …
    Распаковывается net-tools (2.10-0.1ubuntu4) …
    Выбор ранее не выбранного пакета traceroute.
    Подготовка к распаковке …/traceroute_1%3a2.1.5-1_amd64.deb …
    Распаковывается traceroute (1:2.1.5-1) …
    Настраивается пакет tcpdump (4.99.4-3ubuntu4) …
    Настраивается пакет net-tools (2.10-0.1ubuntu4) …
    Настраивается пакет traceroute (1:2.1.5-1) …
    update-alternatives: используется /usr/bin/traceroute.db для предоставления /usr/bin/traceroute (traceroute) в автоматическом 
    режиме
    update-alternatives: используется /usr/bin/traceroute6.db для предоставления /usr/bin/traceroute6 (traceroute6) в автоматическ
    ом режиме
    update-alternatives: используется /usr/bin/lft.db для предоставления /usr/bin/lft (lft) в автоматическом режиме
    update-alternatives: используется /usr/bin/traceproto.db для предоставления /usr/bin/traceproto (traceproto) в автоматическом 
    режиме
    update-alternatives: используется /usr/sbin/tcptraceroute.db для предоставления /usr/sbin/tcptraceroute (tcptraceroute) в авто
    матическом режиме
    Обрабатываются триггеры для man-db (2.12.0-4build2) …
    ```

    d) Установка программы для передачи файлов: 
    ```
    user@ws:~$ sudo apt install -y curl wget
    Чтение списков пакетов… Готово
    Построение дерева зависимостей… Готово
    Чтение информации о состоянии… Готово         
    Уже установлен пакет wget самой новой версии (1.21.4-1ubuntu4.1).
    wget помечен как установленный вручную.
    Следующий пакет устанавливался автоматически и больше не требуется:
    ansible-core git-man hplip-data libdouble-conversion3 liberror-perl libgsoap-2.8.132t64 libhpmud0 libimagequant0 liblzf1
    libmd4c0 libpcre2-16-0 libqt5core5t64 libqt5dbus5t64 libqt5gui5t64 libqt5help5 libqt5network5t64 libqt5opengl5t64
    libqt5printsupport5t64 libqt5qml5 libqt5qmlmodels5 libqt5quick5 libqt5sql5-sqlite libqt5sql5t64 libqt5svg5
    libqt5waylandclient5 libqt5waylandcompositor5 libqt5widgets5t64 libqt5x11extras5 libqt5xml5t64 libraqm0 libsane-hpaio
    libsdl-ttf2.0-0 libsdl1.2debian libtpms0 libvncserver1 libxcb-xinerama0 libxcb-xinput0 printer-driver-hpcups
    printer-driver-postscript-hp python3-argcomplete python3-dnspython python3-jmespath python3-kerberos python3-libcloud
    python3-lockfile python3-ntlm-auth python3-olefile python3-packaging python3-passlib python3-pexpect python3-pil
    python3-ptyprocess python3-requests-ntlm python3-resolvelib python3-selinux python3-simplejson python3-winrm
    python3-xmltodict qt5-gtk-platformtheme qttranslations5-l10n qtwayland5
    Для его удаления используйте «sudo apt autoremove».
    Будут установлены следующие дополнительные пакеты:
    libcurl3t64-gnutls libcurl4t64
    Следующие НОВЫЕ пакеты будут установлены:
    curl
    Следующие пакеты будут обновлены:
    libcurl3t64-gnutls libcurl4t64
    Обновлено 2 пакетов, установлено 1 новых пакетов, для удаления отмечено 0 пакетов, и 148 пакетов не обновлено.
    Необходимо скачать 900 kB архивов.
    После данной операции объём занятого дискового пространства возрастёт на 536 kB.
    Пол:1 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 libcurl4t64 amd64 8.5.0-2ubuntu10.3 [341 kB]
    Пол:2 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 curl amd64 8.5.0-2ubuntu10.3 [227 kB]
    Пол:3 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 libcurl3t64-gnutls amd64 8.5.0-2ubuntu10.3 [333 kB]
    Получено 900 kB за 5с (171 kB/s)              
    (Чтение базы данных … на данный момент установлено 198382 файла и каталога.)
    Подготовка к распаковке …/libcurl4t64_8.5.0-2ubuntu10.3_amd64.deb …
    Распаковывается libcurl4t64:amd64 (8.5.0-2ubuntu10.3) на замену (8.5.0-2ubuntu10.2) …
    Выбор ранее не выбранного пакета curl.
    Подготовка к распаковке …/curl_8.5.0-2ubuntu10.3_amd64.deb …
    Распаковывается curl (8.5.0-2ubuntu10.3) …
    Подготовка к распаковке …/libcurl3t64-gnutls_8.5.0-2ubuntu10.3_amd64.deb …
    Распаковывается libcurl3t64-gnutls:amd64 (8.5.0-2ubuntu10.3) на замену (8.5.0-2ubuntu10.2) …
    Настраивается пакет libcurl4t64:amd64 (8.5.0-2ubuntu10.3) …
    Настраивается пакет libcurl3t64-gnutls:amd64 (8.5.0-2ubuntu10.3) …
    Настраивается пакет curl (8.5.0-2ubuntu10.3) …
    Обрабатываются триггеры для man-db (2.12.0-4build2) …
    Обрабатываются триггеры для libc-bin (2.39-0ubuntu8.3) …

    ```
    e) Установка программы контроля версий: 
    ```
    user@ws:~$ sudo apt install -y git
    Чтение списков пакетов… Готово
    Построение дерева зависимостей… Готово
    Чтение информации о состоянии… Готово         
    Следующие пакеты устанавливались автоматически и больше не требуются:
    ansible-core hplip-data libdouble-conversion3 libgsoap-2.8.132t64 libhpmud0 libimagequant0 liblzf1 libmd4c0 libpcre2-16-0
    libqt5core5t64 libqt5dbus5t64 libqt5gui5t64 libqt5help5 libqt5network5t64 libqt5opengl5t64 libqt5printsupport5t64
    libqt5qml5 libqt5qmlmodels5 libqt5quick5 libqt5sql5-sqlite libqt5sql5t64 libqt5svg5 libqt5waylandclient5
    libqt5waylandcompositor5 libqt5widgets5t64 libqt5x11extras5 libqt5xml5t64 libraqm0 libsane-hpaio libsdl-ttf2.0-0
    libsdl1.2debian libtpms0 libvncserver1 libxcb-xinerama0 libxcb-xinput0 printer-driver-hpcups printer-driver-postscript-hp
    python3-argcomplete python3-dnspython python3-jmespath python3-kerberos python3-libcloud python3-lockfile
    python3-ntlm-auth python3-olefile python3-packaging python3-passlib python3-pexpect python3-pil python3-ptyprocess
    python3-requests-ntlm python3-resolvelib python3-selinux python3-simplejson python3-winrm python3-xmltodict
    qt5-gtk-platformtheme qttranslations5-l10n qtwayland5
    Для их удаления используйте «sudo apt autoremove».
    Предлагаемые пакеты:
    git-daemon-run | git-daemon-sysvinit git-doc git-email git-gui gitk gitweb git-cvs git-mediawiki git-svn
    Следующие НОВЫЕ пакеты будут установлены:
    git
    Обновлено 0 пакетов, установлено 1 новых пакетов, для удаления отмечено 0 пакетов, и 148 пакетов не обновлено.
    Необходимо скачать 3 679 kB архивов.
    После данной операции объём занятого дискового пространства возрастёт на 22,2 MB.
    Пол:1 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 git amd64 1:2.43.0-1ubuntu7.1 [3 679 kB]
    Получено 3 679 kB за 12с (308 kB/s)                                                                                          
    Выбор ранее не выбранного пакета git.
    (Чтение базы данных … на данный момент установлено 198389 файлов и каталогов.)
    Подготовка к распаковке …/git_1%3a2.43.0-1ubuntu7.1_amd64.deb …
    Распаковывается git (1:2.43.0-1ubuntu7.1) …
    Настраивается пакет git (1:2.43.0-1ubuntu7.1) …

    ```
    f) Установка Visual Studio Code:

    Скачал пакет:
    ```
    wget -O code_1.92.1-1723066302_amd64.deb 'https://code.visualstudio.com/sha/download?build=stable&os=linux-deb-x64'
    ```
    Установил:

    ```
    sudo dpkg -i code_1.92.1-1723066302_amd64.deb
    ```
2. Установка Oracle VirtualBox
    a) Добавляем GPG-ключ репозитория: 
    ```
    user@ws:~$ wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
    Warning: apt-key is deprecated. Manage keyring files in trusted.gpg.d instead (see apt-key(8)).
    OK
    ```
    b) Добавляем репозиторий VirtualBox: 
    ```
    user@ws:~$ sudo add-apt-repository "deb [arch=amd64] http://download.virtualbox.org/virtualbox/debian $(lsb_release -cs) contrib"
    Репозиторий: 'deb [arch=amd64] http://download.virtualbox.org/virtualbox/debian noble contrib'
    Описание:
    Archive for codename: noble components: contrib
    Дополнительные сведения: http://download.virtualbox.org/virtualbox/debian
    Добавление репозитория.
    Нажмите [ENTER] для продолжения или Ctrl-C для отмены.
    Добавление записи deb в /etc/apt/sources.list.d/archive_uri-http_download_virtualbox_org_virtualbox_debian-noble.list
    Добавление отключенной записи deb-src в /etc/apt/sources.list.d/archive_uri-http_download_virtualbox_org_virtualbox_debian-noble.list
    Сущ:1 http://security.ubuntu.com/ubuntu noble-security InRelease                                                             
    Сущ:2 http://ru.archive.ubuntu.com/ubuntu noble InRelease                                                                    
    Пол:3 http://download.virtualbox.org/virtualbox/debian noble InRelease [4 428 B]                                             
    Пол:4 http://ru.archive.ubuntu.com/ubuntu noble-updates InRelease [126 kB]                                                   
    Сущ:5 https://packages.microsoft.com/repos/code stable InRelease                                                             
    Сущ:6 https://apt.releases.hashicorp.com noble InRelease                                                                     
    Сущ:7 https://repo.yandex.ru/yandex-browser/deb stable InRelease                                                             
    Сущ:8 http://ru.archive.ubuntu.com/ubuntu noble-backports InRelease                                                
    Пол:9 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 Packages [463 kB]
    Пол:10 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe amd64 Packages [337 kB]
    Пол:11 http://download.virtualbox.org/virtualbox/debian noble/contrib amd64 Packages [1 122 B]                               
    Получено 932 kB за 6с (145 kB/s)                                                                                             
    Чтение списков пакетов… Готово
    W: http://download.virtualbox.org/virtualbox/debian/dists/noble/InRelease: Ключ хранится в унаследованной связке ключей trusted.gpg (/etc/apt/trusted.gpg), подробности см. в разделе DEPRECATION в apt-key(8).
    W: https://apt.releases.hashicorp.com/dists/noble/InRelease: Ключ хранится в унаследованной связке ключей trusted.gpg (/etc/apt/trusted.gpg), подробности см. в разделе DEPRECATION в apt-key(8).

    ```
    c) Обновляем список пакетов: 
    ```
    user@ws:~$ sudo apt update
    Сущ:1 http://security.ubuntu.com/ubuntu noble-security InRelease                                                             
    Сущ:2 http://ru.archive.ubuntu.com/ubuntu noble InRelease                                                                    
    Сущ:3 http://download.virtualbox.org/virtualbox/debian noble InRelease                                                       
    Сущ:4 http://ru.archive.ubuntu.com/ubuntu noble-updates InRelease                                                            
    Сущ:5 http://ru.archive.ubuntu.com/ubuntu noble-backports InRelease                                                          
    Сущ:6 https://packages.microsoft.com/repos/code stable InRelease                                                             
    Сущ:7 https://repo.yandex.ru/yandex-browser/deb stable InRelease                                                             
    Сущ:8 https://apt.releases.hashicorp.com noble InRelease                                                   
    Чтение списков пакетов… Готово                                     
    Построение дерева зависимостей… Готово
    Чтение информации о состоянии… Готово         
    Может быть обновлено 148 пакетов. Запустите «apt list --upgradable» для их показа.
    W: http://download.virtualbox.org/virtualbox/debian/dists/noble/InRelease: Ключ хранится в унаследованной связке ключей trusted.gpg (/etc/apt/trusted.gpg), подробности см. в разделе DEPRECATION в apt-key(8).
    W: https://apt.releases.hashicorp.com/dists/noble/InRelease: Ключ хранится в унаследованной связке ключей trusted.gpg (/etc/apt/trusted.gpg), подробности см. в разделе DEPRECATION в apt-key(8).
 
    ```
    d) Установим VirtualBox: 
    ```
    user@ws:~$ sudo apt install -y virtualbox-7.0
    Чтение списков пакетов… Готово
    Построение дерева зависимостей… Готово
    Чтение информации о состоянии… Готово         
    Следующие пакеты устанавливались автоматически и больше не требуются:
    ansible-core dkms hplip-data libgsoap-2.8.132t64 libhpmud0 libimagequant0 libraqm0 libsane-hpaio libvncserver1
    printer-driver-hpcups printer-driver-postscript-hp python3-argcomplete python3-dnspython python3-jmespath python3-kerberos
    python3-libcloud python3-lockfile python3-ntlm-auth python3-olefile python3-packaging python3-passlib python3-pexpect
    python3-pil python3-ptyprocess python3-requests-ntlm python3-resolvelib python3-selinux python3-simplejson python3-winrm
    python3-xmltodict
    Для их удаления используйте «sudo apt autoremove».
    Следующие пакеты будут УДАЛЕНЫ:
    virtualbox-dkms
    Следующие НОВЫЕ пакеты будут установлены:
    virtualbox-7.0
    Обновлено 0 пакетов, установлено 1 новых пакетов, для удаления отмечено 1 пакетов, и 148 пакетов не обновлено.
    Необходимо скачать 92,6 MB архивов.
    После данной операции объём занятого дискового пространства возрастёт на 214 MB.
    Пол:1 http://download.virtualbox.org/virtualbox/debian noble/contrib amd64 virtualbox-7.0 amd64 7.0.20-163906~Ubuntu~noble [92,6 MB]
    Игн:1 http://download.virtualbox.org/virtualbox/debian noble/contrib amd64 virtualbox-7.0 amd64 7.0.20-163906~Ubuntu~noble   
    Игн:1 http://download.virtualbox.org/virtualbox/debian noble/contrib amd64 virtualbox-7.0 amd64 7.0.20-163906~Ubuntu~noble   
    Игн:1 http://download.virtualbox.org/virtualbox/debian noble/contrib amd64 virtualbox-7.0 amd64 7.0.20-163906~Ubuntu~noble
    Ошб:1 http://download.virtualbox.org/virtualbox/debian noble/contrib amd64 virtualbox-7.0 amd64 7.0.20-163906~Ubuntu~noble
    Время ожидания для соединения истекло [IP: 2.21.188.103 80]
    E: Не удалось получить http://download.virtualbox.org/virtualbox/debian/pool/contrib/v/virtualbox-7.0/virtualbox-7.0_7.0.20-163906%7eUbuntu%7enoble_amd64.deb  Время ожидания для соединения истекло [IP: 2.21.188.103 80]
    E: Не удалось получить некоторые архивы; возможно, нужно запустить apt-get update или попытаться повторить запуск с ключом --fix-missing?
    user@ws:~$ sudo apt install -y --f virtualbox-7.0
    [sudo] пароль для user: 
    E: Параметр командной строки «--f» непонятен в комбинации с другими параметрами
    user@ws:~$ sudo apt install -y -f virtualbox-7.0
    Чтение списков пакетов… Готово
    Построение дерева зависимостей… Готово
    Чтение информации о состоянии… Готово         
    Следующие пакеты устанавливались автоматически и больше не требуются:
    ansible-core dkms hplip-data libgsoap-2.8.132t64 libhpmud0 libimagequant0 libraqm0 libsane-hpaio libvncserver1
    printer-driver-hpcups printer-driver-postscript-hp python3-argcomplete python3-dnspython python3-jmespath python3-kerberos
    python3-libcloud python3-lockfile python3-ntlm-auth python3-olefile python3-packaging python3-passlib python3-pexpect
    python3-pil python3-ptyprocess python3-requests-ntlm python3-resolvelib python3-selinux python3-simplejson python3-winrm
    python3-xmltodict
    Для их удаления используйте «sudo apt autoremove».
    Следующие пакеты будут УДАЛЕНЫ:
    virtualbox-dkms
    Следующие НОВЫЕ пакеты будут установлены:
    virtualbox-7.0
    Обновлено 0 пакетов, установлено 1 новых пакетов, для удаления отмечено 1 пакетов, и 148 пакетов не обновлено.
    Необходимо скачать 92,6 MB архивов.
    После данной операции объём занятого дискового пространства возрастёт на 214 MB.
    Пол:1 http://download.virtualbox.org/virtualbox/debian noble/contrib amd64 virtualbox-7.0 amd64 7.0.20-163906~Ubuntu~noble [92,6 MB]
    Получено 61,8 MB за 7с (8 987 kB/s)                                                                                          
    Предварительная настройка пакетов …
    (Чтение базы данных … на данный момент установлено 199265 файлов и каталогов.)
    Удаляется virtualbox-dkms (7.0.16-dfsg-2ubuntu1) …
    Module virtualbox-7.0.16 for kernel 6.8.0-40-generic (x86_64).
    Before uninstall, this module version was ACTIVE on this kernel.

    vboxdrv.ko.zst:
    - Uninstallation
    - Deleting from: /lib/modules/6.8.0-40-generic/updates/dkms/
    - Original module
    - No original module was found for this module on this kernel.
    - Use the dkms install command to reinstall any previous module version.

    vboxnetadp.ko.zst:
    - Uninstallation
    - Deleting from: /lib/modules/6.8.0-40-generic/updates/dkms/
    - Original module
    - No original module was found for this module on this kernel.
    - Use the dkms install command to reinstall any previous module version.

    vboxnetflt.ko.zst:
    - Uninstallation
    - Deleting from: /lib/modules/6.8.0-40-generic/updates/dkms/
    - Original module
    - No original module was found for this module on this kernel.
    - Use the dkms install command to reinstall any previous module version.
    depmod....
    Module virtualbox-7.0.16 for kernel 6.8.0-41-generic (x86_64).
    Before uninstall, this module version was ACTIVE on this kernel.

    vboxdrv.ko.zst:
    - Uninstallation
    - Deleting from: /lib/modules/6.8.0-41-generic/updates/dkms/
    - Original module
    - No original module was found for this module on this kernel.
    - Use the dkms install command to reinstall any previous module version.

    vboxnetadp.ko.zst:
    - Uninstallation
    - Deleting from: /lib/modules/6.8.0-41-generic/updates/dkms/
    - Original module
    - No original module was found for this module on this kernel.
    - Use the dkms install command to reinstall any previous module version.

    vboxnetflt.ko.zst:
    - Uninstallation
    - Deleting from: /lib/modules/6.8.0-41-generic/updates/dkms/
    - Original module
    - No original module was found for this module on this kernel.
    - Use the dkms install command to reinstall any previous module version.
    depmod....
    Deleting module virtualbox-7.0.16 completely from the DKMS tree.
    Выбор ранее не выбранного пакета virtualbox-7.0.
    (Чтение базы данных … на данный момент установлено 198977 файлов и каталогов.)
    Подготовка к распаковке …/virtualbox-7.0_7.0.20-163906~Ubuntu~noble_amd64.deb …
    Распаковывается virtualbox-7.0 (7.0.20-163906~Ubuntu~noble) …
    Настраивается пакет virtualbox-7.0 (7.0.20-163906~Ubuntu~noble) …
    info: Выбирается GID из диапазона от 100 по 999 ...
    info: Добавляется группа «vboxusers» (GID 124) ...
    vboxdrv.sh: failed: modprobe vboxdrv failed. Please use 'dmesg' to find out why.

    There were problems setting up VirtualBox.  To re-start the set-up process, run
    /sbin/vboxconfig
    as root.  If your system is using EFI Secure Boot you may need to sign the
    kernel modules (vboxdrv, vboxnetflt, vboxnetadp, vboxpci) before you can load
    them. Please see your Linux system's documentation for more information.
    Обрабатываются триггеры для hicolor-icon-theme (0.17-2) …
    Обрабатываются триггеры для gnome-menus (3.36.0-1.1ubuntu3) …
    Обрабатываются триггеры для shared-mime-info (2.4-4) …
    Обрабатываются триггеры для desktop-file-utils (0.27-2build1) …
 
    ```
    e) Установим VirtualBox extension pack: 
    ```
    user@ws:~$ sudo apt install -y virtualbox-ext-pack
    Чтение списков пакетов… Готово
    Построение дерева зависимостей… Готово
    Чтение информации о состоянии… Готово         
    Следующие пакеты устанавливались автоматически и больше не требуются:
    ansible-core dkms hplip-data libgsoap-2.8.132t64 libhpmud0 libimagequant0 libraqm0 libsane-hpaio libvncserver1
    printer-driver-hpcups printer-driver-postscript-hp python3-argcomplete python3-dnspython python3-jmespath python3-kerberos
    python3-libcloud python3-lockfile python3-ntlm-auth python3-olefile python3-packaging python3-passlib python3-pexpect
    python3-pil python3-ptyprocess python3-requests-ntlm python3-resolvelib python3-selinux python3-simplejson python3-winrm
    python3-xmltodict
    Для их удаления используйте «sudo apt autoremove».
    Следующие НОВЫЕ пакеты будут установлены:
    virtualbox-ext-pack
    Обновлено 0 пакетов, установлено 1 новых пакетов, для удаления отмечено 0 пакетов, и 148 пакетов не обновлено.
    Необходимо скачать 12,3 kB архивов.
    После данной операции объём занятого дискового пространства возрастёт на 165 kB.
    Пол:1 http://ru.archive.ubuntu.com/ubuntu noble/multiverse amd64 virtualbox-ext-pack all 7.0.16-1 [12,3 kB]
    Получено 12,3 kB за 0с (223 kB/s)                
    Предварительная настройка пакетов …
    Выбор ранее не выбранного пакета virtualbox-ext-pack.
    (Чтение базы данных … на данный момент установлено 199720 файлов и каталогов.)
    Подготовка к распаковке …/virtualbox-ext-pack_7.0.16-1_all.deb …
    License has already been accepted.
    Распаковывается virtualbox-ext-pack (7.0.16-1) …
    Настраивается пакет virtualbox-ext-pack (7.0.16-1) …
    virtualbox-ext-pack: downloading: https://download.virtualbox.org/virtualbox/7.0.16/Oracle_VM_VirtualBox_Extension_Pack-7.0.16
    .vbox-extpack
    The file will be downloaded into /var/cache/virtualbox-ext-pack
    WARNING: The vboxdrv kernel module is not loaded. Either there is no module
            available for the current kernel (6.8.0-41-generic) or it failed to
            load. Please recompile the kernel module and install it by

            sudo /sbin/vboxconfig

            You will not be able to start VMs until this problem is fixed.
    License accepted.
    0%...10%...20%...30%...40%...50%...60%...70%...80%...90%...100%
    Successfully installed "Oracle VM VirtualBox Extension Pack".
 
    ```


Установка VirtualBox закончена.

3. Установка Hashicorp Vagrant

    a) Добавляем GPG-ключ репозитория: 
    ```
    user@ws:~$ curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
    Warning: apt-key is deprecated. Manage keyring files in trusted.gpg.d instead (see apt-key(8)).
    OK
    ```
    b) Добавляем репозиторий Hashicorp: 
    ```
    user@ws:~$ sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
    Репозиторий: 'deb [arch=amd64] https://apt.releases.hashicorp.com noble main'
    Описание:
    Archive for codename: noble components: main
    Дополнительные сведения: https://apt.releases.hashicorp.com
    Добавление репозитория.
    Нажмите [ENTER] для продолжения или Ctrl-C для отмены.
    Найдена существующая запись deb в /etc/apt/sources.list.d/archive_uri-https_apt_releases_hashicorp_com-noble.list
    Добавление записи deb в /etc/apt/sources.list.d/archive_uri-https_apt_releases_hashicorp_com-noble.list
    Найдена существующая запись deb-src в /etc/apt/sources.list.d/archive_uri-https_apt_releases_hashicorp_com-noble.list
    Добавление отключенной записи deb-src в /etc/apt/sources.list.d/archive_uri-https_apt_releases_hashicorp_com-noble.list
    Сущ:1 http://ru.archive.ubuntu.com/ubuntu noble InRelease
    Пол:2 https://packages.microsoft.com/repos/code stable InRelease [3 590 B]                                                   
    Пол:3 http://ru.archive.ubuntu.com/ubuntu noble-updates InRelease [126 kB]                                                   
    Сущ:4 https://repo.yandex.ru/yandex-browser/deb stable InRelease                                                             
    Сущ:5 http://download.virtualbox.org/virtualbox/debian noble InRelease                                                       
    Сущ:6 https://apt.releases.hashicorp.com noble InRelease                                                                     
    Сущ:7 http://security.ubuntu.com/ubuntu noble-security InRelease                                                   
    Пол:8 https://packages.microsoft.com/repos/code stable/main amd64 Packages [18,2 kB]
    Пол:9 https://packages.microsoft.com/repos/code stable/main armhf Packages [18,3 kB]              
    Пол:10 https://packages.microsoft.com/repos/code stable/main arm64 Packages [18,3 kB]             
    Сущ:11 http://ru.archive.ubuntu.com/ubuntu noble-backports InRelease                                                         
    Получено 185 kB за 6с (29,7 kB/s)                                                                                            
    Чтение списков пакетов… Готово
    W: http://download.virtualbox.org/virtualbox/debian/dists/noble/InRelease: Ключ хранится в унаследованной связке ключей trusted.gpg (/etc/apt/trusted.gpg), подробности см. в разделе DEPRECATION в apt-key(8).
    W: https://apt.releases.hashicorp.com/dists/noble/InRelease: Ключ хранится в унаследованной связке ключей trusted.gpg (/etc/apt/trusted.gpg), подробности см. в разделе DEPRECATION в apt-key(8).
    N: Отсутствует "Signed-By" в записи sources.list(5) для 'http://ru.archive.ubuntu.com/ubuntu'

    ```
    c) Обновляем список пакетов: 
    ```
    user@ws:~$ sudo apt update
    Сущ:1 http://ru.archive.ubuntu.com/ubuntu noble InRelease                                                                    
    Сущ:2 http://security.ubuntu.com/ubuntu noble-security InRelease                                                             
    Сущ:3 http://download.virtualbox.org/virtualbox/debian noble InRelease                                                       
    Пол:4 http://ru.archive.ubuntu.com/ubuntu noble-updates InRelease [126 kB]                                                   
    Сущ:5 https://packages.microsoft.com/repos/code stable InRelease                                                             
    Сущ:6 https://repo.yandex.ru/yandex-browser/deb stable InRelease                                                             
    Сущ:7 https://apt.releases.hashicorp.com noble InRelease                                                           
    Сущ:8 http://ru.archive.ubuntu.com/ubuntu noble-backports InRelease        
    Получено 126 kB за 3с (48,5 kB/s)         
    Чтение списков пакетов… Готово
    Построение дерева зависимостей… Готово
    Чтение информации о состоянии… Готово         
    Может быть обновлено 147 пакетов. Запустите «apt list --upgradable» для их показа.
    W: http://download.virtualbox.org/virtualbox/debian/dists/noble/InRelease: Ключ хранится в унаследованной связке ключей trusted.gpg (/etc/apt/trusted.gpg), подробности см. в разделе DEPRECATION в apt-key(8).
    W: https://apt.releases.hashicorp.com/dists/noble/InRelease: Ключ хранится в унаследованной связке ключей trusted.gpg (/etc/apt/trusted.gpg), подробности см. в разделе DEPRECATION в apt-key(8).
    N: Отсутствует "Signed-By" в записи sources.list(5) для 'http://ru.archive.ubuntu.com/ubuntu'

    ```
    d) Установим Vagrant: 
    ```
    user@ws:~$ sudo apt install -y vagrant
    [sudo] пароль для user: 
    Чтение списков пакетов… Готово
    Построение дерева зависимостей… Готово
    Чтение информации о состоянии… Готово         
    Следующие пакеты устанавливались автоматически и больше не требуются:
    7zip ansible-core cabextract dkms fonts-wine hplip-data icoutils libcapi20-3t64 libgsoap-2.8.132t64 libhpmud0
    libimagequant0 libmspack0t64 libodbc2 libosmesa6 libraqm0 libsane-hpaio libvncserver1 libwine libwxbase3.2-1t64
    libwxgtk-gl3.2-1t64 libwxgtk3.2-1t64 libz-mingw-w64 p7zip-full printer-driver-hpcups printer-driver-postscript-hp
    python3-argcomplete python3-dnspython python3-jmespath python3-kerberos python3-libcloud python3-lockfile python3-natsort
    python3-ntlm-auth python3-olefile python3-packaging python3-passlib python3-pexpect python3-pil python3-ptyprocess
    python3-requests-ntlm python3-resolvelib python3-selinux python3-simplejson python3-winrm python3-wxgtk4.0
    python3-xmltodict wine wine64
    Для их удаления используйте «sudo apt autoremove».
    Следующие НОВЫЕ пакеты будут установлены:
    vagrant
    Обновлено 0 пакетов, установлено 1 новых пакетов, для удаления отмечено 0 пакетов, и 164 пакетов не обновлено.
    Необходимо скачать 150 MB архивов.
    После данной операции объём занятого дискового пространства возрастёт на 384 MB.
    Пол:1 https://apt.releases.hashicorp.com noble/main amd64 vagrant amd64 2.4.1-1 [150 MB]
    Получено 96,6 MB за 13мин 0с (124 kB/s)                                                                                      
    Выбор ранее не выбранного пакета vagrant.
    (Чтение базы данных … на данный момент установлено 202439 файлов и каталогов.)
    Подготовка к распаковке …/vagrant_2.4.1-1_amd64.deb …
    Распаковывается vagrant (2.4.1-1) …
    Настраивается пакет vagrant (2.4.1-1) …

    ```
    e) Проверим версию Vagrant: 
    ```
    user@ws:~$ vagrant version
    Installed Version: 2.4.1
    Latest Version: 2.4.1

    ```

4. Установка Ansible
    a) Устанавливаем Ansible: 
    ```
    user@ws:~$ sudo apt install -y ansible
    [sudo] пароль для user: 
    Попробуйте ещё раз.
    [sudo] пароль для user: 
    Чтение списков пакетов… Готово
    Построение дерева зависимостей… Готово
    Чтение информации о состоянии… Готово         
    Следующие пакеты устанавливались автоматически и больше не требуются:
    7zip cabextract dkms fonts-wine hplip-data icoutils libcapi20-3t64 libgsoap-2.8.132t64 libhpmud0 libimagequant0
    libmspack0t64 libodbc2 libosmesa6 libraqm0 libsane-hpaio libvncserver1 libwine libwxbase3.2-1t64 libwxgtk-gl3.2-1t64
    libwxgtk3.2-1t64 libz-mingw-w64 p7zip-full printer-driver-hpcups printer-driver-postscript-hp python3-natsort
    python3-olefile python3-pexpect python3-pil python3-ptyprocess python3-wxgtk4.0 wine wine64
    Для их удаления используйте «sudo apt autoremove».
    Предлагаемые пакеты:
    cowsay sshpass
    Следующие НОВЫЕ пакеты будут установлены:
    ansible
    Обновлено 0 пакетов, установлено 1 новых пакетов, для удаления отмечено 0 пакетов, и 164 пакетов не обновлено.
    Необходимо скачать 16,4 MB архивов.
    После данной операции объём занятого дискового пространства возрастёт на 294 MB.
    Пол:1 http://ru.archive.ubuntu.com/ubuntu noble/universe amd64 ansible all 9.2.0+dfsg-0ubuntu5 [16,4 MB]
    Получено 16,4 MB за 51с (321 kB/s)                                                                                           
    Выбор ранее не выбранного пакета ansible.
    (Чтение базы данных … на данный момент установлено 210511 файлов и каталогов.)
    Подготовка к распаковке …/ansible_9.2.0+dfsg-0ubuntu5_all.deb …
    Распаковывается ansible (9.2.0+dfsg-0ubuntu5) …
    Настраивается пакет ansible (9.2.0+dfsg-0ubuntu5) …
    Обрабатываются триггеры для man-db (2.12.0-4build2) …

    ```
    b) Проверяем версию Ansible: 
    ```
    user@ws:~$ ansible --version
    ansible [core 2.16.3]
    config file = None
    configured module search path = ['/home/user/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
    ansible python module location = /usr/lib/python3/dist-packages/ansible
    ansible collection location = /home/user/.ansible/collections:/usr/share/ansible/collections
    executable location = /usr/bin/ansible
    python version = 3.12.3 (main, Jul 31 2024, 17:43:48) [GCC 13.2.0] (/usr/bin/python3)
    jinja version = 3.1.2
    libyaml = True
    ```

    ## Проверка работы Vagrant.

    Создадал каталог setupws и перешел в него: 
    ```
    mkdir setupws && cd setupws
    ```
    Запросил Vagrantfile из Vagrant cloud : 
    ```
    user@ws:~/Рабочий стол/OTUS/TASKS/0/setupws$ vagrant init ubuntu/focal64
    A `Vagrantfile` has been placed in this directory. You are now
    ready to `vagrant up` your first virtual environment! Please read
    the comments in the Vagrantfile as well as documentation on
    `vagrantup.com` for more information on using Vagrant.
    ```
    Проверил содержимое Vagrantfile:
    ```
    # -*- mode: ruby -*-
    # vi: set ft=ruby :

    # All Vagrant configuration is done below. The "2" in Vagrant.configure
    # configures the configuration version (we support older styles for
    # backwards compatibility). Please don't change it unless you know what
    # you're doing.
    Vagrant.configure("2") do |config|
    # The most common configuration options are documented and commented below.
    # For a complete reference, please see the online documentation at
    # https://docs.vagrantup.com.

    # Every Vagrant development environment requires a box. You can search for
    # boxes at https://vagrantcloud.com/search.
    config.vm.box = "ubuntu/focal64"

    # Disable automatic box update checking. If you disable this, then
    # boxes will only be checked for updates when the user runs
    # `vagrant box outdated`. This is not recommended.
    # config.vm.box_check_update = false

    # Create a forwarded port mapping which allows access to a specific port
    # within the machine from a port on the host machine. In the example below,
    # accessing "localhost:8080" will access port 80 on the guest machine.
    # NOTE: This will enable public access to the opened port
    # config.vm.network "forwarded_port", guest: 80, host: 8080

    # Create a forwarded port mapping which allows access to a specific port
    # within the machine from a port on the host machine and only allow access
    # via 127.0.0.1 to disable public access
    # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

    # Create a private network, which allows host-only access to the machine
    # using a specific IP.
    # config.vm.network "private_network", ip: "192.168.33.10"

    # Create a public network, which generally matched to bridged network.
    # Bridged networks make the machine appear as another physical device on
    # your network.
    # config.vm.network "public_network"

    # Share an additional folder to the guest VM. The first argument is
    # the path on the host to the actual folder. The second argument is
    # the path on the guest to mount the folder. And the optional third
    # argument is a set of non-required options.
    # config.vm.synced_folder "../data", "/vagrant_data"

    # Disable the default share of the current code directory. Doing this
    # provides improved isolation between the vagrant box and your host
    # by making sure your Vagrantfile isn't accessible to the vagrant box.
    # If you use this you may want to enable additional shared subfolders as
    # shown above.
    # config.vm.synced_folder ".", "/vagrant", disabled: true

    # Provider-specific configuration so you can fine-tune various
    # backing providers for Vagrant. These expose provider-specific options.
    # Example for VirtualBox:
    #
    # config.vm.provider "virtualbox" do |vb|
    #   # Display the VirtualBox GUI when booting the machine
    #   vb.gui = true
    #
    #   # Customize the amount of memory on the VM:
    #   vb.memory = "1024"
    # end
    #
    # View the documentation for the provider you are using for more
    # information on available options.

    # Enable provisioning with a shell script. Additional provisioners such as
    # Ansible, Chef, Docker, Puppet and Salt are also available. Please see the
    # documentation for more information about their specific syntax and use.
    # config.vm.provision "shell", inline: <<-SHELL
    #   apt-get update
    #   apt-get install -y apache2
    # SHELL
    end
    ```

    Запустил виртуальню машину с настройками по умолчанию:
    ```
    user@ws:~/Рабочий стол/OTUS/TASKS/0/setupws$ vagrant up
    Bringing machine 'default' up with 'virtualbox' provider...
    ==> default: Box 'ubuntu/focal64' could not be found. Attempting to find and install...
        default: Box Provider: virtualbox
        default: Box Version: >= 0
    ==> default: Loading metadata for box 'ubuntu/focal64'
        default: URL: https://vagrantcloud.com/api/v2/vagrant/ubuntu/focal64
    ==> default: Adding box 'ubuntu/focal64' (v20240821.0.0) for provider: virtualbox
        default: Downloading: https://vagrantcloud.com/ubuntu/boxes/focal64/versions/20240821.0.0/providers/virtualbox/unknown/vagrant.box
    ==> default: Box download is resuming from prior download progress
    Download redirected to host: cloud-images.ubuntu.com
    ==> default: Successfully added box 'ubuntu/focal64' (v20240821.0.0) for 'virtualbox'!
    ==> default: Importing base box 'ubuntu/focal64'...
    ==> default: Matching MAC address for NAT networking...
    ==> default: Checking if box 'ubuntu/focal64' version '20240821.0.0' is up to date...
    ==> default: Setting the name of the VM: setupws_default_1724770503731_95399
    Vagrant is currently configured to create VirtualBox synced folders with
    the `SharedFoldersEnableSymlinksCreate` option enabled. If the Vagrant
    guest is not trusted, you may want to disable this option. For more
    information on this option, please refer to the VirtualBox manual:

    https://www.virtualbox.org/manual/ch04.html#sharedfolders

    This option can be disabled globally with an environment variable:

    VAGRANT_DISABLE_VBOXSYMLINKCREATE=1

    or on a per folder basis within the Vagrantfile:

    config.vm.synced_folder '/host/path', '/guest/path', SharedFoldersEnableSymlinksCreate: false
    ==> default: Clearing any previously set network interfaces...
    ==> default: Preparing network interfaces based on configuration...
        default: Adapter 1: nat
    ==> default: Forwarding ports...
        default: 22 (guest) => 2222 (host) (adapter 1)
    ==> default: Running 'pre-boot' VM customizations...
    ==> default: Booting VM...
    ==> default: Waiting for machine to boot. This may take a few minutes...
        default: SSH address: 127.0.0.1:2222
        default: SSH username: vagrant
        default: SSH auth method: private key
        default: Warning: Connection reset. Retrying...
        default: Warning: Remote connection disconnect. Retrying...
        default: 
        default: Vagrant insecure key detected. Vagrant will automatically replace
        default: this with a newly generated keypair for better security.
        default: 
        default: Inserting generated public key within guest...
        default: Removing insecure key from the guest if it's present...
        default: Key inserted! Disconnecting and reconnecting using new SSH key...
    ==> default: Machine booted and ready!
    ==> default: Checking for guest additions in VM...
        default: The guest additions on this VM do not match the installed version of
        default: VirtualBox! In most cases this is fine, but in rare cases it can
        default: prevent things such as shared folders from working properly. If you see
        default: shared folder errors, please make sure the guest additions within the
        default: virtual machine match the version of VirtualBox you have installed on
        default: your host and reload your VM.
        default: 
        default: Guest Additions Version: 6.1.50
        default: VirtualBox Version: 7.0
    ==> default: Mounting shared folders...
        default: /vagrant => /home/user/Рабочий стол/OTUS/TASKS/0/setupws

    ```
    Подключился к виртуальной машине по ssh:
    ```
    user@ws:~/Рабочий стол/OTUS/TASKS/0/setupws$ vagrant ssh
    Welcome to Ubuntu 20.04.6 LTS (GNU/Linux 5.4.0-193-generic x86_64)

    * Documentation:  https://help.ubuntu.com
    * Management:     https://landscape.canonical.com
    * Support:        https://ubuntu.com/pro

    System information as of Tue Aug 27 14:58:04 UTC 2024

    System load:  0.05              Processes:               121
    Usage of /:   3.6% of 38.70GB   Users logged in:         0
    Memory usage: 20%               IPv4 address for enp0s3: 10.0.2.15
    Swap usage:   0%


    Expanded Security Maintenance for Applications is not enabled.

    0 updates can be applied immediately.

    Enable ESM Apps to receive additional future security updates.
    See https://ubuntu.com/esm or run: sudo pro status

    New release '22.04.3 LTS' available.
    Run 'do-release-upgrade' to upgrade to it.


    vagrant@ubuntu-focal:~$
    ```
    Закрыл подключение по ssh и удалил виртуальную машину:
    ```
    vagrant@ubuntu-focal:~$ exit
    logout
    user@ws:~/Рабочий стол/OTUS/TASKS/0/setupws$ vagrant destroy
        default: Are you sure you want to destroy the 'default' VM? [y/N] y
    ==> default: Forcing shutdown of VM...
    ==> default: Destroying VM and associated drives...
    ```
Внес изменения в Vagrantfile:
- пробросил 80й порт с гостевой машины в  хостовую на 8080й
- указал количество ОЗУ и ядер процессора
- в цикл первоначальной настройки ОС включил установку Вэб-сервера Apache2
    ```
    Vagrant.configure("2") do |config|

    # boxes at https://vagrantcloud.com/search.
    config.vm.box = "ubuntu/focal64"
    config.vm.box_version = "20240821.0.0" 
    # NOTE: This will enable public access to the opened port
    config.vm.network "forwarded_port", guest: 80, host: 8080

    #
    config.vm.provider "virtualbox" do |vb|
    
    #   # Customize the amount of memory on the VM:
        vb.memory = "2048"
        vb.cpus = "2"
        end
    
    # documentation for more information about their specific syntax and use.
    config.vm.provision "shell", inline: <<-SHELL
        apt-get update
        apt-get install -y apache2
    SHELL
    end
```
Внес изменения в Vagrantfile, изменил количество ядер процессора, выполнил vagrant reload и vagrant provision:

```
    user@ws:~/Рабочий стол/OTUS/TASKS/0/setupws$ vagrant up
    Bringing machine 'default' up with 'virtualbox' provider...
    ==> default: Importing base box 'ubuntu/focal64'...
    ==> default: Matching MAC address for NAT networking...
    ==> default: Checking if box 'ubuntu/focal64' version '20240821.0.0' is up to date...
    ==> default: Setting the name of the VM: setupws_default_1724920277024_70218
    ==> default: Clearing any previously set network interfaces...
    ==> default: Preparing network interfaces based on configuration...
        default: Adapter 1: nat
    ==> default: Forwarding ports...
        default: 80 (guest) => 8080 (host) (adapter 1)
        default: 22 (guest) => 2222 (host) (adapter 1)
    ==> default: Running 'pre-boot' VM customizations...
    ==> default: Booting VM...
    ==> default: Waiting for machine to boot. This may take a few minutes...
        default: SSH address: 127.0.0.1:2222
        default: SSH username: vagrant
        default: SSH auth method: private key
        default: Warning: Connection reset. Retrying...
        default: Warning: Remote connection disconnect. Retrying...
        default: 
        default: Vagrant insecure key detected. Vagrant will automatically replace
        default: this with a newly generated keypair for better security.
        default: 
        default: Inserting generated public key within guest...
        default: Removing insecure key from the guest if it's present...
        default: Key inserted! Disconnecting and reconnecting using new SSH key...
    ==> default: Machine booted and ready!
    ==> default: Checking for guest additions in VM...
        default: The guest additions on this VM do not match the installed version of
        default: VirtualBox! In most cases this is fine, but in rare cases it can
        default: prevent things such as shared folders from working properly. If you see
        default: shared folder errors, please make sure the guest additions within the
        default: virtual machine match the version of VirtualBox you have installed on
        default: your host and reload your VM.
        default: 
        default: Guest Additions Version: 6.1.50
        default: VirtualBox Version: 7.0
    ==> default: Mounting shared folders...
        default: /vagrant => /home/user/Рабочий стол/OTUS/TASKS/0/setupws
    ==> default: Running provisioner: shell...
        default: Running: inline script
        default: Hit:1 http://archive.ubuntu.com/ubuntu focal InRelease
        default: Get:2 http://archive.ubuntu.com/ubuntu focal-updates InRelease [128 kB]
        default: Get:3 http://security.ubuntu.com/ubuntu focal-security InRelease [128 kB]
        default: Get:4 http://archive.ubuntu.com/ubuntu focal-backports InRelease [128 kB]
        default: Get:5 http://archive.ubuntu.com/ubuntu focal/universe amd64 Packages [8628 kB]
        default: Get:6 http://security.ubuntu.com/ubuntu focal-security/main amd64 Packages [3163 kB]
        default: Get:7 http://archive.ubuntu.com/ubuntu focal/universe Translation-en [5124 kB]
        default: Get:8 http://archive.ubuntu.com/ubuntu focal/universe amd64 c-n-f Metadata [265 kB]
        default: Get:9 http://archive.ubuntu.com/ubuntu focal/multiverse amd64 Packages [144 kB]
        default: Get:10 http://archive.ubuntu.com/ubuntu focal/multiverse Translation-en [104 kB]
        default: Get:11 http://archive.ubuntu.com/ubuntu focal/multiverse amd64 c-n-f Metadata [9136 B]
        default: Get:12 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 Packages [3534 kB]
        default: Get:13 http://archive.ubuntu.com/ubuntu focal-updates/main Translation-en [547 kB]
        default: Get:14 http://security.ubuntu.com/ubuntu focal-security/main Translation-en [467 kB]
        default: Get:15 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 c-n-f Metadata [17.7 kB]
        default: Get:16 http://archive.ubuntu.com/ubuntu focal-updates/restricted amd64 Packages [3199 kB]
        default: Get:17 http://security.ubuntu.com/ubuntu focal-security/restricted amd64 Packages [3080 kB]
        default: Get:18 http://archive.ubuntu.com/ubuntu focal-updates/restricted Translation-en [448 kB]
        default: Get:19 http://archive.ubuntu.com/ubuntu focal-updates/universe amd64 Packages [1220 kB]
        default: Get:20 http://archive.ubuntu.com/ubuntu focal-updates/universe Translation-en [294 kB]
        default: Get:21 http://archive.ubuntu.com/ubuntu focal-updates/universe amd64 c-n-f Metadata [27.8 kB]
        default: Get:22 http://archive.ubuntu.com/ubuntu focal-updates/multiverse amd64 Packages [27.1 kB]
        default: Get:23 http://archive.ubuntu.com/ubuntu focal-updates/multiverse Translation-en [7936 B]
        default: Get:24 http://archive.ubuntu.com/ubuntu focal-updates/multiverse amd64 c-n-f Metadata [616 B]
        default: Get:25 http://archive.ubuntu.com/ubuntu focal-backports/main amd64 Packages [45.7 kB]
        default: Get:26 http://archive.ubuntu.com/ubuntu focal-backports/main Translation-en [16.3 kB]
        default: Get:27 http://archive.ubuntu.com/ubuntu focal-backports/main amd64 c-n-f Metadata [1420 B]
        default: Get:28 http://archive.ubuntu.com/ubuntu focal-backports/restricted amd64 c-n-f Metadata [116 B]
        default: Get:29 http://archive.ubuntu.com/ubuntu focal-backports/universe amd64 Packages [25.0 kB]
        default: Get:30 http://security.ubuntu.com/ubuntu focal-security/restricted Translation-en [431 kB]
        default: Get:31 http://archive.ubuntu.com/ubuntu focal-backports/universe Translation-en [16.3 kB]
        default: Get:32 http://archive.ubuntu.com/ubuntu focal-backports/universe amd64 c-n-f Metadata [880 B]
        default: Get:33 http://archive.ubuntu.com/ubuntu focal-backports/multiverse amd64 c-n-f Metadata [116 B]
        default: Get:34 http://security.ubuntu.com/ubuntu focal-security/universe amd64 Packages [1001 kB]
        default: Get:35 http://security.ubuntu.com/ubuntu focal-security/universe Translation-en [212 kB]
        default: Get:36 http://security.ubuntu.com/ubuntu focal-security/universe amd64 c-n-f Metadata [21.0 kB]
        default: Get:37 http://security.ubuntu.com/ubuntu focal-security/multiverse amd64 Packages [24.8 kB]
        default: Get:38 http://security.ubuntu.com/ubuntu focal-security/multiverse Translation-en [5968 B]
        default: Get:39 http://security.ubuntu.com/ubuntu focal-security/multiverse amd64 c-n-f Metadata [540 B]
        default: Fetched 32.5 MB in 7s (4817 kB/s)
        default: Reading package lists...
        default: Reading package lists...
        default: Building dependency tree...
        default: Reading state information...
        default: The following additional packages will be installed:
        default:   apache2-bin apache2-data apache2-utils libapr1 libaprutil1
        default:   libaprutil1-dbd-sqlite3 libaprutil1-ldap libjansson4 liblua5.2-0 ssl-cert
        default: Suggested packages:
        default:   apache2-doc apache2-suexec-pristine | apache2-suexec-custom www-browser
        default:   openssl-blacklist
        default: The following NEW packages will be installed:
        default:   apache2 apache2-bin apache2-data apache2-utils libapr1 libaprutil1
        default:   libaprutil1-dbd-sqlite3 libaprutil1-ldap libjansson4 liblua5.2-0 ssl-cert
        default: 0 upgraded, 11 newly installed, 0 to remove and 5 not upgraded.
        default: Need to get 1875 kB of archives.
        default: After this operation, 8121 kB of additional disk space will be used.
        default: Get:1 http://archive.ubuntu.com/ubuntu focal/main amd64 libapr1 amd64 1.6.5-1ubuntu1 [91.4 kB]
        default: Get:2 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libaprutil1 amd64 1.6.1-4ubuntu2.2 [85.1 kB]
        default: Get:3 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libaprutil1-dbd-sqlite3 amd64 1.6.1-4ubuntu2.2 [10.5 kB]
        default: Get:4 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libaprutil1-ldap amd64 1.6.1-4ubuntu2.2 [8752 B]
        default: Get:5 http://archive.ubuntu.com/ubuntu focal/main amd64 libjansson4 amd64 2.12-1build1 [28.9 kB]
        default: Get:6 http://archive.ubuntu.com/ubuntu focal/main amd64 liblua5.2-0 amd64 5.2.4-1.1build3 [106 kB]
        default: Get:7 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 apache2-bin amd64 2.4.41-4ubuntu3.21 [1189 kB]
        default: Get:8 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 apache2-data all 2.4.41-4ubuntu3.21 [159 kB]
        default: Get:9 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 apache2-utils amd64 2.4.41-4ubuntu3.21 [84.7 kB]
        default: Get:10 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 apache2 amd64 2.4.41-4ubuntu3.21 [95.6 kB]
        default: Get:11 http://archive.ubuntu.com/ubuntu focal/main amd64 ssl-cert all 1.0.39 [17.0 kB]
        default: dpkg-preconfigure: unable to re-open stdin: No such file or directory
        default: Fetched 1875 kB in 1s (2808 kB/s)
        default: Selecting previously unselected package libapr1:amd64.
    (Reading database ... 63783 files and directories currently installed.)
        default: Preparing to unpack .../00-libapr1_1.6.5-1ubuntu1_amd64.deb ...
        default: Unpacking libapr1:amd64 (1.6.5-1ubuntu1) ...
        default: Selecting previously unselected package libaprutil1:amd64.
        default: Preparing to unpack .../01-libaprutil1_1.6.1-4ubuntu2.2_amd64.deb ...
        default: Unpacking libaprutil1:amd64 (1.6.1-4ubuntu2.2) ...
        default: Selecting previously unselected package libaprutil1-dbd-sqlite3:amd64.
        default: Preparing to unpack .../02-libaprutil1-dbd-sqlite3_1.6.1-4ubuntu2.2_amd64.deb ...
        default: Unpacking libaprutil1-dbd-sqlite3:amd64 (1.6.1-4ubuntu2.2) ...
        default: Selecting previously unselected package libaprutil1-ldap:amd64.
        default: Preparing to unpack .../03-libaprutil1-ldap_1.6.1-4ubuntu2.2_amd64.deb ...
        default: Unpacking libaprutil1-ldap:amd64 (1.6.1-4ubuntu2.2) ...
        default: Selecting previously unselected package libjansson4:amd64.
        default: Preparing to unpack .../04-libjansson4_2.12-1build1_amd64.deb ...
        default: Unpacking libjansson4:amd64 (2.12-1build1) ...
        default: Selecting previously unselected package liblua5.2-0:amd64.
        default: Preparing to unpack .../05-liblua5.2-0_5.2.4-1.1build3_amd64.deb ...
        default: Unpacking liblua5.2-0:amd64 (5.2.4-1.1build3) ...
        default: Selecting previously unselected package apache2-bin.
        default: Preparing to unpack .../06-apache2-bin_2.4.41-4ubuntu3.21_amd64.deb ...
        default: Unpacking apache2-bin (2.4.41-4ubuntu3.21) ...
        default: Selecting previously unselected package apache2-data.
        default: Preparing to unpack .../07-apache2-data_2.4.41-4ubuntu3.21_all.deb ...
        default: Unpacking apache2-data (2.4.41-4ubuntu3.21) ...
        default: Selecting previously unselected package apache2-utils.
        default: Preparing to unpack .../08-apache2-utils_2.4.41-4ubuntu3.21_amd64.deb ...
        default: Unpacking apache2-utils (2.4.41-4ubuntu3.21) ...
        default: Selecting previously unselected package apache2.
        default: Preparing to unpack .../09-apache2_2.4.41-4ubuntu3.21_amd64.deb ...
        default: Unpacking apache2 (2.4.41-4ubuntu3.21) ...
        default: Selecting previously unselected package ssl-cert.
        default: Preparing to unpack .../10-ssl-cert_1.0.39_all.deb ...
        default: Unpacking ssl-cert (1.0.39) ...
        default: Setting up libapr1:amd64 (1.6.5-1ubuntu1) ...
        default: Setting up libjansson4:amd64 (2.12-1build1) ...
        default: Setting up ssl-cert (1.0.39) ...
        default: Setting up liblua5.2-0:amd64 (5.2.4-1.1build3) ...
        default: Setting up apache2-data (2.4.41-4ubuntu3.21) ...
        default: Setting up libaprutil1:amd64 (1.6.1-4ubuntu2.2) ...
        default: Setting up libaprutil1-ldap:amd64 (1.6.1-4ubuntu2.2) ...
        default: Setting up libaprutil1-dbd-sqlite3:amd64 (1.6.1-4ubuntu2.2) ...
        default: Setting up apache2-utils (2.4.41-4ubuntu3.21) ...
        default: Setting up apache2-bin (2.4.41-4ubuntu3.21) ...
        default: Setting up apache2 (2.4.41-4ubuntu3.21) ...
        default: Enabling module mpm_event.
        default: Enabling module authz_core.
        default: Enabling module authz_host.
        default: Enabling module authn_core.
        default: Enabling module auth_basic.
        default: Enabling module access_compat.
        default: Enabling module authn_file.
        default: Enabling module authz_user.
        default: Enabling module alias.
        default: Enabling module dir.
        default: Enabling module autoindex.
        default: Enabling module env.
        default: Enabling module mime.
        default: Enabling module negotiation.
        default: Enabling module setenvif.
        default: Enabling module filter.
        default: Enabling module deflate.
        default: Enabling module status.
        default: Enabling module reqtimeout.
        default: Enabling conf charset.
        default: Enabling conf localized-error-pages.
        default: Enabling conf other-vhosts-access-log.
        default: Enabling conf security.
        default: Enabling conf serve-cgi-bin.
        default: Enabling site 000-default.
        default: Created symlink /etc/systemd/system/multi-user.target.wants/apache2.service → /lib/systemd/system/apache2.service.
        default: Created symlink /etc/systemd/system/multi-user.target.wants/apache-htcacheclean.service → /lib/systemd/system/apache-htcacheclean.service.
        default: Processing triggers for ufw (0.36-6ubuntu1.1) ...
        default: Processing triggers for systemd (245.4-4ubuntu3.23) ...
        default: Processing triggers for man-db (2.9.1-1) ...
        default: Processing triggers for libc-bin (2.31-0ubuntu9.16) ...
    user@ws:~/Рабочий стол/OTUS/TASKS/0/setupws$ vagrant reload
    ==> default: Attempting graceful shutdown of VM...
    ==> default: Checking if box 'ubuntu/focal64' version '20240821.0.0' is up to date...
    ==> default: Clearing any previously set forwarded ports...
    ==> default: Clearing any previously set network interfaces...
    ==> default: Preparing network interfaces based on configuration...
        default: Adapter 1: nat
    ==> default: Forwarding ports...
        default: 80 (guest) => 8080 (host) (adapter 1)
        default: 22 (guest) => 2222 (host) (adapter 1)
    ==> default: Running 'pre-boot' VM customizations...
    ==> default: Booting VM...
    ==> default: Waiting for machine to boot. This may take a few minutes...
        default: SSH address: 127.0.0.1:2222
        default: SSH username: vagrant
        default: SSH auth method: private key
    ==> default: Machine booted and ready!
    ==> default: Checking for guest additions in VM...
        default: The guest additions on this VM do not match the installed version of
        default: VirtualBox! In most cases this is fine, but in rare cases it can
        default: prevent things such as shared folders from working properly. If you see
        default: shared folder errors, please make sure the guest additions within the
        default: virtual machine match the version of VirtualBox you have installed on
        default: your host and reload your VM.
        default: 
        default: Guest Additions Version: 6.1.50
        default: VirtualBox Version: 7.0
    ==> default: Mounting shared folders...
        default: /vagrant => /home/user/Рабочий стол/OTUS/TASKS/0/setupws
    ==> default: Machine already provisioned. Run `vagrant provision` or use the `--provision`
    ==> default: flag to force provisioning. Provisioners marked to run always will still run.
    user@ws:~/Рабочий стол/OTUS/TASKS/0/setupws$ vagrant provision
    ==> default: Running provisioner: shell...
        default: Running: inline script
        default: Hit:1 http://security.ubuntu.com/ubuntu focal-security InRelease
        default: Hit:2 http://archive.ubuntu.com/ubuntu focal InRelease
        default: Hit:3 http://archive.ubuntu.com/ubuntu focal-updates InRelease
        default: Hit:4 http://archive.ubuntu.com/ubuntu focal-backports InRelease
        default: Reading package lists...
        default: Reading package lists...
        default: Building dependency tree...
        default: Reading state information...
        default: apache2 is already the newest version (2.4.41-4ubuntu3.21).
        default: 0 upgraded, 0 newly installed, 0 to remove and 5 not upgraded.
    ```