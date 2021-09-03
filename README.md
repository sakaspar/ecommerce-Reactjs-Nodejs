# 1. Run Backend

```
$ npm install
$ npm start
```

# 2. Run Frontend

```
# open new terminal
$ cd frontend
$ npm install
$ npm start
```

# 3. Create Admin User

- Run this on chrome: http://localhost:5000/api/users/createadmin
- It returns admin email and password

# 4. Login

- Run http://localhost:3000/signin
- Enter admin email and password and click signin

# 5. Create Products

- Run http://localhost:3000/products
- Click create product and enter product info

## Support LIB Core-JS

https://github.com/zloirock/core-js

# Part 6- Order Details Screen

It shows all details about an order includeing shipping, payments and order items. Also it is possible for admin to manage orders like set them as delivered.

# Part 7- Connect to PayPal

This parts create PaypalButton component to show paypal payment button on the screen.
when users click on it, they will be redirected to paypal website to make the payment.
after payment users will be redirected to details page of the order.

# Part 8- Manage Order Screen

This is an admin page to manage list of orders. Admin can delete an order or set it as delivered.

# Part 9- User Profile Screen

When user click on thier name on the header menu, this page appears. It consists of two sections. First an profile update form and second order history.

# Part 10- Filter and Sort Products

In the home page, right after header, there is a filter bar to filter products based on their name and description. also it is possible to sort product based on prices and arrivals.


# Part 11- Rate and Review Products

This part shows list of reviews by users for each products. also it provides a form to enter rating and review for every single product. also it update the avg rating of each product by user ratings.

1. index.html
2. link fontawesome
3. Rating.js
4. create stars based on props.value
5. show text based on props.text
6. index.css
7. style rating, span color gold and last span to gray, link text to blue
8. HomeScreen.js
9. use Rating component
10. ProductScreen.js
11. use Rating component, wrap it in anchor#reviews
12. list reviews after product details
13. create new review form to get rating and reviews
14. index.css
15. style reviews
16. ProductScreen.js
17. implement submitHandler
18. productActions.js
19. create saveProductReview(productId, review)
20. productConstants.js
21. create product review constants
22. productReducers.js
23. create productReviewSaveReducer
24. store.js
25. add productReviewSaveReducer
26. backend
27. productRoute.js
28. router.post('/:id/reviews')
29. save review in product.reviews
30. update avg rating

# Part 12- Upload Product Images On Local Server

Admin shoud be able to uploads photos from their computer. This section is about uploading images on local server ans aws s3 cloud server.

1. npm install multer
2. routes/uploadRoute.js
3. import express and multer
4. create disk storage with Date.now().jpg as filename
5. set upload as multer({ storage })
6. router.post('/', upload.single('image'))
7. return req.file.path
8. server.js
9. app.use('/api/uploads',uploadRoute)
10. ProductsScreen.js
11. create state hook for uploading
12. create input image file and onChange handler
13. define handleUploadImage function
14. prepare file for upload
15. axios post file as multipart/form-data
16. set image and set uploading
17. check result


# Summary

we have made an eCommerce website like Amazon. Feel free to change this project based on your needs and add it to your portfolio.
Big Thanks to zloirock 
git: https://github.com/zloirock 
