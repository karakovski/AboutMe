## задание 1

```<?php

// первая переменная
$first = trim(fgets(STDIN));

// вторая переменная
$second = trim(fgets(STDIN));

// проверяем тип первой переменной
if (!is_numeric($first))
fwrite(STDERR, 'Введите, пожалуйста, число'.PHP_EOL);

// проверяем тип второй переменной
if (!is_numeric($second))
fwrite(STDERR, 'Введите, пожалуйста, число'.PHP_EOL);

// на ноль делить нельзя
if ($second === 0) {
fwrite(STDERR, 'Делить на 0 нельзя'.PHP_EOL); }
else {

  // деление
$number = $first / $second;

  // вывод результата
echo(STDOUT.$number.PHP_EOL);
  
}
?>```


## задание 2


```<?php

// получаем имя
$name = trim(fgets(STDIN));

// получаем отчество
$fathersname = trim(fgets(STDIN));

// получаем фамилию
$surname = trim(fgets(STDIN));

// делаем с заглавной буквы имя
$n_name = mb_ucfirst($name);

// делаем с заглавной буквы отчество
$n_fathersname = mb_ucfirst($fathersname);

// делаем с заглавной буквы фамилию
$n_surname = mb_ucfirst($surname);

// первая переменная
$fullName = "$n_name $n_fathersname $n_surname";

// вторая переменная
$fio = mb_substr($n_name, 0, 1).mb_substr($n_fathersname, 0, 1).mb_substr($n_surname, 0, 1);

// третья переменная
$surnameAndInitials = $n_surname.' '.mb_substr($n_name, 0, 1).'.'.mb_substr($n_fathersname, 0, 1).'.';

// вывод результата
echo(STDOUT.$fullName.PHP_EOL);
echo(STDOUT.$fio.PHP_EOL);
echo(STDOUT.$surnameAndInitials.PHP_EOL);

?>```

