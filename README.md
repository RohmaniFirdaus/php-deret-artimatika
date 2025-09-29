# php-deret-artimatika
Program ini ditulis dengan PHP untuk membantu menyelesaikan soal tes psikotes deret angka. Idenya simpel: ada beberapa urutan angka dengan pola tertentu, lalu program otomatis mencari dan melengkapi angka selanjutnya.
<?php
$a = [4, 6, 9, 13, 18];
$selisih = 2;
for ($i = count($a); $i < 7; $i++) {
    $selisih++;
    $a[] = end($a) + $selisih;
}
$b = [2, 2, 3, 3, 4];
while (count($b) < 7) {
    $b[] = ceil(count($b)/2) + 1;
}
$c = [1, 9, 2, 10, 3];
$n1 = 4; 
$n2 = 11; 
while (count($c) < 7) {
    if (count($c) % 2 == 1) {
        $c[] = $n2++;
    } else {
        $c[] = $n1++;
    }
}
echo "a. " . implode(", ", $a) . PHP_EOL;
echo "b. " . implode(", ", $b) . PHP_EOL;
echo "c. " . implode(", ", $c) . PHP_EOL;
?>
