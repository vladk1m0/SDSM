# VPLS Kompella Mode \(BGP\)

Проблему поиска соседей решил Кирити Компелла — сотрудник Juniper. Он отталкивался от тех же критериев, но решил, что [MBGP](http://lookmeup.linkmeup.ru/#term238), опробованный на L3VPN, подойдёт лучше на роль протокола распределения меток.  
Схема обмена маршрутной информацией, однажды расширенная до VPNv4 маршрутов, вполне может быть применена и для доставкой меток VPLS.  
Механизм Route Target поможет с автоопределением соседей.  
А рут-рефлекторы решат задачу реализации полносвязной топологии, которая остро стоит в Martini Mode.

Другое название VPLS Kompella-mode — VPLS Auto-Discovery, потому что именно это является его качественным отличием от Martini. Также вы можете услышать VPLS BGP Signaling.

Control Plane выполняет здесь две основные функции:  
— Обнаружение соседей  
— Передача маршрутной информации и обмен метками.

