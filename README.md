#Подключение 
- Загружаем файл yii.phar в папку там где лежит фремворк 
- В index.php заменяем подключение yii.php|yiilite.php на
	$yii="phar://".dirname(dirname(__FILE__)).'/yii.phar/yii.php'; 
	(Если структура директорий из каробки то нужно изминить путь до phar архива) 
- сохраняем и запускаем.

Если возникает ошибка 
 Необходимый для отображения asset "phar:///home/yoyoCMF/yii.phar/web/js/source" не существует.
 то в файле настройки прописываем 
 'clientScript'=>array
                (
                    ...
                    //устанавливаем нашу директорию со скриптами(ЕСЛИ ИСПОЛЬЗУЕМ YII.PHAR)
                    'coreScriptUrl'=>DIRECTORY_SEPARATOR.'js'.DIRECTORY_SEPARATOR,
                ),

 Другие проблемы не замечаны.