## Replace old mob_drop_item for better view

This script is for developers of private metin2 servers. 
Script simply replace awkward group names with new ones by searching the mob id trough mob_names file 
and past it to the group name in mob_drop_item file.

In my case mob_drop_item is in .cpp format, but you can also use any other text format. 
In script I used **unidecode** only for visual purposes - to save group names in universal way.

### Technologies:
- [Python 3.11.8 64-bit](https://www.python.org/downloads/release/python-3118/)
- [unidecode](https://github.com/avian2/unidecode)

### Expected file structure:
mob_drop_item.cpp
```
Group	���ֹ���_Ǫ���θ����
{
	Type	kill
	Mob	134
	kill_drop	400
	1	5110	1	25	10
	2	290	1	15	10
}

Group	���ֹ���_���������
{
	Type	kill
	Mob	138
 [...]
```

### Result:
mob_drop_item_generated.cpp
```
Group	Przekl_Nieb_Alfa_Wilk
{
	Type	kill
	Mob	134
	kill_drop	400
	1	5110	1	25	10
	2	290	1	15	10
}


Group	Przeklety_Czerw_Dzik
{
	Type	kill
	Mob	138
[...]
```
