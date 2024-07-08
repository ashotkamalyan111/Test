№1
HTTP Method: GET
Endpoint: “/market.yandex.ru/recommendations”
Headers:
{ 
"Authorization": "Bearer {token}", 
"Content-Type": "application/json" 
}
Json-ответ:
{
  "recommendations": [
    {
      "product_id": 1,
      "name": "Наручные часы CASIO COLLECTION LTP-VT02BL 3A",
      "price": 3400,
      “old_price”: 4539,
     “favorites”: false,
      "image_url": "https://example.com/images/watchcasio.jpg",
    },
    {
      "product_id": 2,
      "name": "Стеллаж для книг KM LOFT Ромбо черный/дуб вотан",
      "price": 9407,
      “old_price”: 42900,
      “favorites”: false,
      "image_url": "https://example.com/images/watch_Casio.jpg",
    },
{
      "product_id": 3,
      "name": "Полка настенная ChoodWood 60x20 см из массива дерева карагач",
      "price": 2520,
      “old_price”: 8918,
      “favorites”: false,
      "image_url": "https://example.com/images/choodWood_shelf.jpg",
    },
{
      "product_id": 4,
      "name": "Тумба прикроватная из МДФ Белая ноги золото, 50x50x40 см",
      "price": 14725,
      “old_price”: 20000
      “favorites”: false,
      "image_url": "https://example.com/images/pedestal_whiteGold.jpg",
    },

№2
User -> YandexMarket: Open recommendations screen
YandexMarket -> API: GET /market.yandex.ru/recommendations
API -> Database: Fetch recommended products
Database --> API: Return recommended products
API --> YandexMarket: Return JSON response with recommendations
YandexMarket -> User: Display recommended products
User -> YandexMarket: Click on a specific product
YandexMarket -> API: GET /market.yandex.ru/product/{product_id}
API -> Database: Fetch product details
Database --> API: Return product details
API --> YandexMarket: Return JSON response with product details
YandexMarket -> User: Display product details

№3
Отношение многие-ко-многим
Students
---------
student_id (PK)
name
Courses
---------
course_id (PK)
title

StudentCourses
---------
student_id (PK, FK)
course_id (PK, FK)
enrollment_date

Отношение один-к-одному
Users
---------
user_id (PK)
username

Profiles
---------
profile_id (PK, FK)
user_id (FK)
description

N4
1. C
2. C
3. C
4. D 
5. C
