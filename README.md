# homework3.dart
void main() {
  int age = 16;
  bool isStudent = true, isBlocked = false;

  if (isBlocked) {
    print('Доступ запрещён');
  } else if (age >= 18) {
    print('Доступ разрешён');
  } else if (isStudent) {
    print('Доступ разрешён для студента');
  } else {
    print('Доступ запрещён');
  }

  List<int> numbers = [12, 5, 8, 21, 16, 3, 10];
  int sum = 0, even = 0, odd = 0, max = numbers[0];

  for (int n in numbers) {
    print(n);
    sum += n;
    n % 2 == 0 ? even++ : odd++;
    if (n > 10) print('больше 10: $n');
    if (n > max) max = n;
  }
  print('Сумма: $sum, чётных: $even, нечётных: $odd, максимум: $max');

  List<int> grades = [85, 42, 90, 67, 55, 100, 38];
  int total = 0, passed = 0, failed = 0;

  for (int g in grades) {
    String result = g >= 90
        ? 'Отлично'
        : g >= 70
            ? 'Хорошо'
            : g >= 50
                ? 'Удовлетворительно'
                : 'Неудовлетворительно';
    print('$g — $result');
    total += g;
    g >= 50 ? passed++ : failed++;
  }

  double avg = total / grades.length;
  print('Сдали: $passed, не сдали: $failed, средний балл: ${avg.toStringAsFixed(2)}');
  print(avg >= 70 && passed > failed
      ? 'Группа успешно сдала экзамен'
      : 'Результаты группы необходимо улучшить');

  List<String> products = ['Хлеб', 'Молоко', 'Яйца'];
  List<int> prices = [40, 80, 120];
  int cart = 0;

  for (int i = 0; i < products.length; i++) {
    print('${products[i]} — ${prices[i]} сом');
    cart += prices[i];
  }

  int discount = cart > 500 ? 20 : (cart > 200 ? 10 : 0);
  print('Сумма: $cart, скидка: $discount%, итого: ${cart * (100 - discount) / 100} сом');
}
