## 01-variables

Challenge: Create a Person Object
-โค้ดส่วนนี้สร้าง object ชื่อ student เพื่อเก็บข้อมูลของนักเรียนในรูปแบบที่เป็นโครงสร้างเดียวกัน
เช่น ชื่อ นามสกุล อายุ เกรดเฉลี่ย รายวิชาที่เรียน และสถานะการใช้งาน
พร้อมทั้งสร้าง method ภายใน object เพื่อใช้รวมชื่อ–นามสกุล (getFullName)
และแสดงข้อมูลนักเรียนทั้งหมด (getInfo) โดยใช้ this เพื่ออ้างถึงข้อมูลภายใน object เดียวกัน

# ผลลัพธ์

=== Variables & Data Types Practice ===

Constants:
MAX_USERS: 100
PI: 3.14159

Variable (let):
count after increment: 2

=== Primitive Data Types ===
Numbers: 25 5.9 -10
Strings: John Doe
Booleans: isStudent: true isTeacher: false
null: null
undefined: undefined

=== Object Data Types ===
Array: [ 'apple', 'banana', 'orange' ]
First fruit: apple
Array length: 3
Object: { name: 'John', age: 25, city: 'Bangkok', isStudent: true }
Person name: John
Person age: 25

=== typeof Operator ===
typeof 25: number
typeof 'hello': string
typeof true: boolean
typeof undefined: undefined
typeof []: object
typeof {}: object
typeof (() => {}): function

=== Type Coercion ===
'5' + 2: 52
'5' - 2: 3
'5' \* 2: 10
true + 1: 2

Explicit coercion:
String(25): 25
Number('25'): 25
Boolean(1): true
Boolean(0): false
Boolean(''): false
Boolean('hello'): true

=== Challenge: Person Object ===
Student object:
{
firstName: 'Alice',
lastName: 'Smith',
age: 20,
gpa: 3.8,
courses: [ 'HTML', 'CSS', 'JavaScript' ],
isActive: true,
getFullName: [Function: getFullName],
getInfo: [Function: getInfo]
}
Full name: Alice Smith
Info: Alice Smith, Age: 20, GPA: 3.8
Courses: HTML, CSS, JavaScript

=== Truthy vs Falsy ===
Falsy values:
0: false
"": false
null: false
undefined: false
false: false
NaN: false

Truthy values:
1: true
hello: true
true: true
[]: true
{}: true
() => {}: true

✅ Activity 1 completed!

## 02-functions

Returning Objects
-โค้ดส่วนนี้เป็นฟังก์ชันที่คืนค่าออกมาเป็น object แทนการคืนค่าเพียงค่าเดียว
ทำให้สามารถส่งข้อมูลหลายอย่างกลับไปพร้อมกันได้ เช่น ผลการตรวจสอบว่า valid
หรือไม่ และข้อความอธิบายผลลัพธ์ ซึ่งเหมาะกับงานประเภท validation หรือการตรวจสอบเงื่อนไขต่าง ๆ
Function as Parameter (Callback)
-โค้ดส่วนนี้แสดงแนวคิดของ callback โดยการส่งฟังก์ชันหนึ่งเข้าไปเป็นพารามิเตอร์ของอีกฟังก์ชันหนึ่ง
ทำให้ฟังก์ชันหลักสามารถเรียกใช้ logic ที่ส่งเข้ามาได้ภายหลัง ซึ่งช่วยให้โค้ดมีความยืดหยุ่น
และสามารถเปลี่ยนพฤติกรรมการทำงานได้โดยไม่ต้องแก้โค้ดหลัก

# ผลลัพธ์

=== Functions & Arrow Functions Practice ===

Function Declaration:
Hello, John!
Hello, Alice!

Function Expression:
add(5, 3): 8
add(10, 20): 30

Arrow Function (full syntax):
multiply(4, 5): 20
Arrow Function (shorthand):
square(5): 25
double(10): 20
getRandom(): 38

Default Parameters:
Anonymous is 0 years old from Unknown
John is 0 years old from Unknown
John is 25 years old from Unknown
John is 25 years old from Bangkok

Rest Parameters:
sum(1, 2, 3): 6
sum(5, 10, 15, 20): 50
sum(): 0
sumWithReduce(2, 4, 6, 8): 20

Destructuring Parameters:
Alice, 22 years old, from Chiang Mai

Validation Function:
{ valid: false, message: 'Email is required' }
{ valid: false, message: 'Invalid email format' }
{ valid: false, message: 'Missing domain extension' }
{ valid: true, message: 'Email is valid' }

Returning Objects:
{
firstName: 'John',
lastName: 'Doe',
age: 30,
email: 'john.doe@example.com',
getFullName: [Function: getFullName],
getAge: [Function: getAge]
}
Email: john.doe@example.com
Full name: John Doe

Callback Function:
Original: [ 1, 2, 3, 4, 5 ]
Doubled: [ 2, 4, 6, 8, 10 ]
Squared: [ 1, 4, 9, 16, 25 ]

Challenge: Calculator
5 + 3 = 8
10 - 4 = 6
6 \* 7 = 42
20 / 4 = 5
2 ^ 10 = 1024
Using operate('add', 5, 3) = 8

✅ Activity 2 completed!

## 03-control-flow

Short-Circuit Evaluation
-โค้ดส่วนนี้ใช้ตัวดำเนินการ && และ || เพื่อควบคุมการทำงานของโปรแกรมโดยไม่ต้องเขียน if ให้ยาว
เมื่อเงื่อนไขด้านหน้าตัดสินผลลัพธ์ได้แล้ว JavaScript จะไม่ประมวลผลเงื่อนไขถัดไป ช่วยลดโค้ดและเพิ่มความกระชับ
Form Validation
-โค้ดส่วนนี้ใช้เงื่อนไข if เพื่อตรวจสอบความถูกต้องของข้อมูลที่ผู้ใช้กรอกเข้ามา เช่น ค่าว่าง รูปแบบอีเมลไม่ถูกต้อง หรือข้อมูลไม่ครบ
ก่อนที่จะอนุญาตให้ส่งฟอร์มหรือดำเนินการขั้นตอนถัดไป เพื่อป้องกันข้อมูลผิดพลาด

# ผลลัพธ์

=== Control Flow & Logic Practice ===

Age Classification:
Age 5: Child
Age 15: Teenager
Age 25: Adult
Age 65: Senior

Day Names:
Day 1: Monday
Day 2: Tuesday
Day 3: Wednesday
Day 4: Thursday
Day 5: Friday
Day 6: Saturday
Day 7: Sunday
Day 8: Unknown day

Weekday/Weekend:
Monday (1): Weekday
Saturday (6): Weekend

Logical Operators:
Can drive: true
Is special age: true
Is not adult: false

Short-Circuit Evaluation:
User name: John
User profile: undefined

Grading System:
Score 95: Grade A
Score 85: Grade B
Score 75: Grade C
Score 65: Grade D
Score 55: Grade F

Form Validation:
Valid user: { isValid: true, errors: [] }
Invalid user: {
isValid: false,
errors: [
'Name must be at least 3 characters',
'Valid email is required',
'Must be 18 or older',
'Password must be at least 6 characters',
'Must agree to terms'
]
}

Challenge: Traffic Light
red: 🛑🛑 STOP
yellow: 🟨🟨 SLOW DOWN
green: 🟢🟢 GO
blue: ❓ INVALID COLOR

✅ Activity 3 completed!

## 04-loops

Chaining Methods
-โค้ดส่วนนี้ใช้การเรียกเมธอดของ array ต่อเนื่องกันหลายตัว เช่น filter, map และ reduce เพื่อคัดกรอง แปลงค่า
และสรุปผลข้อมูลในลำดับเดียว ทำให้โค้ดอ่านง่ายและเข้าใจลำดับการประมวลผลได้ชัดเจน
Challenge: Student Grades
-โค้ดส่วนนี้ประมวลผลข้อมูลคะแนนของนักเรียนจาก array โดยใช้ลูปหรือ array methods
เพื่อคำนวณค่าเฉลี่ย แปลงคะแนนเป็นเกรด และสรุปผลการเรียนตามเงื่อนไขที่กำหนด

# ผลลัพธ์

=== Loops & Array Methods Practice ===

For loop (0-4):
i = 0
i = 1
i = 2
i = 3
i = 4

While loop (count down):
5...
4...
3...
2...
1...
Blastoff! 🚀🚀

For...of loop (fruits):

- apple
- banana
- orange

For...in loop (person properties):
name: John
age: 25
city: Bangkok

forEach (with index):
0: apple
1: banana
2: orange

map - transform elements:
Original: [ 1, 2, 3, 4, 5 ]
Doubled: [ 2, 4, 6, 8, 10 ]
Squared: [ 1, 4, 9, 16, 25 ]
As strings: [ 'Number: 1', 'Number: 2', 'Number: 3', 'Number: 4', 'Number: 5' ]

filter - select elements:
Even numbers: [ 2, 4 ]
Odd numbers: [ 1, 3, 5 ]
Numbers > 2: [ 3, 4, 5 ]

reduce - accumulate:
Sum: 15
Product: 120
Concatenated: 12345
Word count: { apple: 3, banana: 1, orange: 1 }

Method chaining:
Even numbers squared: 2²=4, 4²=16, 6²=36, 8²=64, 10²=100
Average: 30

Challenge: Student Analysis
Students: [
{ name: 'Alice', score: 95 },
{ name: 'Bob', score: 75 },
{ name: 'Charlie', score: 85 },
{ name: 'Diana', score: 92 },
{ name: 'Eve', score: 88 }
]
Names: Alice, Bob, Charlie, Diana, Eve
High scorers: Alice (95), Charlie (85), Diana (92), Eve (88)
Class average: 87.00
Top scorer: Alice (95)
Summary (sorted):
Alice: 95 (A)
Diana: 92 (A)
Eve: 88 (B)
Charlie: 85 (B)
Bob: 75 (C)

✅ Activity 4 completed!

## 05-integration

Activity 5: Integration – Quiz Application
-โค้ดส่วนนี้เป็นการนำความรู้จากหลายหัวข้อ เช่น ตัวแปร ฟังก์ชัน เงื่อนไข ลูป และ array methods มาทำงานร่วมกัน เพื่อสร้างระบบแบบทดสอบที่สามารถแสดงคำถาม
รับคำตอบ ตรวจสอบความถูกต้อง และคำนวณคะแนนรวมได้อย่างเป็นขั้นตอน

# ผลลัพธ์

🎯🎯 === QUIZ APPLICATION === 🎯🎯

QUIZ RESULTS:
────────────────────────────────────────────────────────────
Q1: What is 5 + 3?
Your answer: 9
Correct answer: 8
❌ WRONG

Q2: What is the capital of Thailand?
Your answer: Chiang Mai
Correct answer: Bangkok
❌ WRONG

Q3: What is the largest planet?
Your answer: Jupiter
✅ CORRECT

Q4: What is 2^8?
Your answer: 128
Correct answer: 256
❌ WRONG

Q5: Which is NOT a JavaScript data type?
Your answer: symbol
Correct answer: class
❌ WRONG

────────────────────────────────────────────────────────────
FINAL SCORE: 1/5 (20.0%)
GRADE: F

FEEDBACK:
💪💪 Keep practicing. You'll improve!

📊📊 STATISTICS:
Total questions: 5
Correct: 1
Incorrect: 4
Success rate: 20.0%

Answer breakdown:
✅ Correct: 1
❌ Incorrect: 4

✅ All activities completed!
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
