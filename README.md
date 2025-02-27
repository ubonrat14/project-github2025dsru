# project-github2025dsru
เขียน code text สำหรับสร้างวงจรไฟฟ้ากับสัญญาณไฟจราจรด้วย Tinkercad.com มีไฟแดง ไฟเหลือง ไฟเขียน ให้สั่งเปิดและปิด เป็นช่วงเวลาที่เท่าๆกัน การกระทำนี้วนซ้ำทำบน Arduino uno 3R
เพื่อสร้างวงจรไฟจราจรบน Tinkercad โดยใช้ Arduino Uno, คุณสามารถเขียนโปรแกรมต่อไปนี้ ซึ่งจะทำให้ไฟแดง, ไฟเหลือง, และไฟเขียวทำงานในช่วงเวลาเท่ากันและวนซ้ำไปเรื่อย ๆ:
ส่วนประกอบที่ต้องใช้:
Arduino Uno
LED 3 ดวง (แดง, เหลือง, เขียว)
ตัวต้านทาน 3 ตัว (220 โอห์ม)
สาย Jumper และบอร์ดแปะ (Breadboard)
การเชื่อมต่อ:
โค้ด:
ไฟแดง (LED) ต่อที่ขา 13 ของ Arduino
ไฟเหลือง (LED) ต่อที่ขา 12 ของ Arduino
ไฟเขียว (LED) ต่อที่ขา 11 ของ Arduino
ตัวต้านทาน 220 โอห์มเชื่อมระหว่างขา GND ของ LED กับ GND ของบอร์ด

// กำหนดขา LED
int redLight = 13;
int yellowLight = 12;
int greenLight = 11;

void setup() {
  // กำหนดขา LED เป็น OUTPUT
  pinMode(redLight, OUTPUT);
  pinMode(yellowLight, OUTPUT);
  pinMode(greenLight, OUTPUT);
}

void loop() {
  // ไฟแดงเปิด, ไฟอื่นปิด
  digitalWrite(redLight, HIGH);
  digitalWrite(yellowLight, LOW);
  digitalWrite(greenLight, LOW);
  delay(5000);  // รอ 5 วินาที (ไฟแดง)

  // ไฟเหลืองเปิด, ไฟอื่นปิด
  digitalWrite(redLight, LOW);
  digitalWrite(yellowLight, HIGH);
  digitalWrite(greenLight, LOW);
  delay(2000);  // รอ 2 วินาที (ไฟเหลือง)

  // ไฟเขียวเปิด, ไฟอื่นปิด
  digitalWrite(redLight, LOW);
  digitalWrite(yellowLight, LOW);
  digitalWrite(greenLight, HIGH);
  delay(5000);  // รอ 5 วินาที (ไฟเขียว)
}
