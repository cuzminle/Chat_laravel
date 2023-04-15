<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>


Данный проект представляет из себя простой чат c приватными каналами. В вебсокеты использовались через Pusher.
<p>Отправа и обработка сообщений реалиозвана в 
app/events/SendMessageEvent.php
app/http/Controllers/MessageController.php, 
app/http/Requests/Message/StoreRequest.php,
app/http/Resources/Message/MessageResource.php
resources/js/Pages/Message/index.vue
</p>

<p>
Отправка лайков реализована в
app/events/SendLikeEvent.php
app/http/Controllers/UserController.php
app/http/Requests/SendLikeRequest.php
resources/js/Pages/User/show.vue
</p>

