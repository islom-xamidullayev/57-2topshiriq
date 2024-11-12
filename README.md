# savollarga javoblar 

## 1 Single threading va multi threading deganda nimani tushunasiz?

Single Threading – bu bir vaqtning o'zida bitta vazifani bajaradigan dasturlash modeli.

Multi Threading – bu bir vaqtning o'zida bir nechta jarayonlarni bajara olish imkoniyatiga ega dasturlash modeli.


## 2 Synxron va asynxron dasturlash deganda nimani tushunasiz va ularni farqi nimada?
Synxron dasturlash – bunda vazifalar ketma-ket bajariladi, ya'ni bir vazifa tugamasdan boshqa vazifa boshlanmaydi. Bunda dasturning bir qismi boshqa bir vazifaning tugashini kutadi. Masalan, synxron kodingizda qatorlar birma-bir bajariladi.


Asynxron dasturlash – bunda vazifalar bir-biriga bog‘liq bo‘lmagan holda bajariladi, ya'ni bir vazifa kutayotgan vaqtda boshqasi bajarilib ketishi mumkin. JavaScriptning asynxron funksiyalari (async/await yoki callbacks) bunga misol bo'la oladi. Bu usulda kutish vaqtlarini kamaytirish uchun parallel ishlashni ta’minlaydi.


 ##  3 JavaScript event loop nima?

 Event Loop – bu JavaScript dasturlash muhiti ishlaydigan asosiy mexanizmlardan biri. JavaScript single-threaded bo'lgani uchun bir vaqtning o'zida birgina vazifani bajaradi. Event loop asynxron vazifalarni boshqaradi va Call Stack (chaqirish steki) va Task Queue (vazifalar navbati) bilan ishlaydi. Asynxron vazifalar (masalan, setTimeout, API chaqiruvlari) tugagach, ularni Task Queue ga qo'shadi va Event Loop ularni Call Stackga joylashtiradi.


## 4 Microtask Queue va Task Queue (Macrotask queue ham deyiladi) ni farqi nimada?

Microtask Queue – bunda mikro-vazifalar joylashtiriladi. Promises yoki MutationObserver kabi asynxron jarayonlar mikrotask navbatiga tushadi. Ular odatda event loopda yuqori ustuvorlikka ega va Task Queue dagi vazifalardan oldin bajariladi.

Task Queue (Macrotask Queue) – bu setTimeout, setInterval, yoki DOM hodisalari (eventlar) kabi asynxron jarayonlar tushadigan navbat. Task Queue dagi vazifalar Microtask Queue tugaganidan keyin bajariladi.

## 5 Kod qaysi ketma ketligida ishlaydi ?

  console.log("1")  // 1


setTimeout(function t2() {  // 6
    console.log("2")
}, 100);

setTimeout(function t3() {  // 4
    console.log("0")
}, 0)

Promise.resolve().then(function t3(){  // 3
  console.log("3")

})

fetch("https://google.com ").then(() => {  // 5
      console.log("google")                  
})

  console.log("4")  // 2


j:  1430 google 2

## 6 WEB APP nima ?

Web app (web dastur) – bu foydalanuvchilar internet orqali foydalanishi mumkin bo'lgan dasturiy ta'minot. Web applar brauzer orqali ishlaydi va ko'pincha server tomonida ishlov beriladi. Ular mobil ilovalar kabi o'rnatilmaydi, balki internet orqali kiriladi, bu esa ulardan istalgan qurilma va platformadan foydalanish imkoniyatini beradi.

Masalan, Gmail, Google Docs, Facebook, yoki Telegram Web kabi dasturlar – web applarga misoldir.

