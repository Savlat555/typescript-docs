# 📘 TypeScript (TS) — Umumiy Dokumentatsiya

## 1. TypeScript nima?
**TypeScript** — bu Microsoft tomonidan yaratilgan dasturlash tili bo'lib, u JavaScriptning kengaytirilgan (superset) ko'rinishidir. U JavaScriptga **statik tiplash (static typing)** xususiyatini qo'shadi.
* Brauzerlar TypeScriptni to'g'ridan-to'g'ri tushunmaydi, shuning uchun kod **Compiler (`tsc`)** yordamida oddiy JavaScriptga o'giriladi.
* **Afzalligi:** Xatolarni kod ishga tushmasidan oldin (yozish jarayonida) aniqlash imkonini beradi.

---

## 2. Asosiy Tiplar (Basic Types)
O'zgaruvchilarga aniq ma'lumot turlarini biriktirish:

```typescript
let ism: string = "Javohir";        // Matn
let yosh: number = 17;              // Son (butun va kasr)
let talabami: boolean = true;       // Mantiqiy (true/false)
let bosh: null = null;              // Bo'sh qiymat
let aniqmas: undefined = undefined; // Qiymat berilmagan
let harQanday: any = "Salom";       // Har qanday tip (ishlatish tavsiya etilmaydi)


let sonlar: number[] = [1, 2, 3, 4];
let ismlar: Array<string> = ["Ali", "Vali"];

let foydalanuvchi: [string, number] = ["Jasur", 20];

let id: string | number;
id = 101;
id = "A-101";

let holat: "kutilmoqda" | "tasdiqlandi" | "rad_etildi";
holat = "tasdiqlandi";

interface Student {
  id: number;
  name: string;
  isActive?: boolean; // '?' belgisi ixtiyoriy maydon ekanligini bildiradi
}

const student1: Student = {
  id: 1,
  name: "Sardor"
};

type Point = {
  x: number;
  y: number;
};

function qoshish(a: number, b: number): number {
  return a + b;
}

// Hech narsa qaytarmaydigan funksiya (void)
function xabarChiqar(matn: string): void {
  console.log(matn);
}


enum Role {
  Admin = "ADMIN",
  User = "USER",
  Guest = "GUEST"
}

let meningRolim: Role = Role.Admin;

function qaytar<T>(qiymat: T): T {
  return qiymat;
}

let matn = qaytar<string>("Salom");
let raqam = qaytar<number>(123);
