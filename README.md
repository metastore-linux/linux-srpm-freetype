# Информация

SPEC-файл для создания RPM-пакета **freetype**.

## Установка

1. Подключить репозиторий **METASTORE**: `dnf copr enable metastore/freetype`.
2. Установить пакет: `dnf install freetype`.
3. Сохранить `/etc/fonts/local.conf` или `~/.fonts.conf` со следующим содержимым:

```
<?xml version='1.0'?>
<!DOCTYPE fontconfig SYSTEM 'fonts.dtd'>
<fontconfig>
	<match target="font">
		<edit mode="assign" name="rgba">
			<const>rgb</const>
		</edit>
	</match>
	<match target="font">
		<edit mode="assign" name="hinting">
			<bool>true</bool>
		</edit>
	</match>
	<match target="font">
		<edit mode="assign" name="hintstyle">
			<const>hintslight</const>
		</edit>
	</match>
	<match target="font">
		<edit mode="assign" name="antialias">
			<bool>true</bool>
		</edit>
	</match>
	<match target="font">
		<edit mode="assign" name="lcdfilter">
			<const>lcddefault</const>
		</edit>
	</match>
</fontconfig>
```

## Авторы

- [**Kitsune Solar**](https://kitsune.solar/) - мейнтейнер.

## Ссылки

- [**METASTORE**](https://metastore.pro/) - хранилище открытых проектов [**METADATA**](https://metadata.foundation/).
- [**METADATA.Foundation**](https://metadata.foundation/) - поддержка и разработка открытых проектов.
