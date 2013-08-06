utilities
=========

Различные небольшие функции нужные в быту



            /**
             * Функция возвращает правильное окончание слова, в зависимости от количества ($num)
             * @param $num
             * @param $str1
             * @param $str2
             * @param $str3
             * @param isShow
             * @returns {string}
             */
             
            function get_correct_str ($num, $str1, $str2, $str3, isShow) {
                var _num = isShow? $num + ' ' : '';
                $val = $num % 100;

                if ($val > 10 && $val < 20) {
                    return _num + $str3;
                }
                else {
                    $val = $num % 10;
                    if ($val == 1) {
                        return _num + $str1;
                    } else if ($val > 1 && $val < 5) {
                        return _num + $str2;
                    } else {
                        return _num + $str3;
                    }
                }
            }
