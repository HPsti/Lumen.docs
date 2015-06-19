# Шифрование

- [Введение](#introduction)
- [Использование](#basic-usage)

<a name="introduction"></a>
## Введение

Lumen предоставляет механизм стойкого шифрования AES на основе PHP расширения Mcrypt.

<a name="basic-usage"></a>
## Использование

#### Шифрование значения

	$encrypted = Crypt::encrypt('secret');

> **Примечание:** Обязательно укажите строку из 32 случайных символов в опции key `APP_KEY` файла config/app.php. В противном случае, зашифрованные значения будет легко расшифровать.

#### Дешифровка значения

	$decrypted = Crypt::decrypt($encryptedValue);

#### Установка алгоритма шифрования и режима работы

Вы можете установить алгоритм шифрования и режим работы:

	Crypt::setMode('ctr');

	Crypt::setCipher($cipher);
 