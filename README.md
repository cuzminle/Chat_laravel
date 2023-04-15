<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>


Данный проект представляет из себя простой чат c приватными каналами. В вебсокеты использовались через Pusher.
<p>Отправа и обработка сообщений реалиозвана в 
<p>app/events/SendMessageEvent.php</p>
<p>app/http/Controllers/MessageController.php,</p> 
<p>app/http/Requests/Message/StoreRequest.php,</p>
<p>app/http/Resources/Message/MessageResource.php</p>
<p>resources/js/Pages/Message/index.vue</p>
</p>

<p>
Отправка лайков реализована в
<p>app/events/SendLikeEvent.php</p>
<p>app/http/Controllers/UserController.php</p>
<p>app/http/Requests/SendLikeRequest.php</p>
<p>resources/js/Pages/User/show.vue</p>
</p>

