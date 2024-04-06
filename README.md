# Laravel Reverb: Real-Time Chat App

> In March of 2024, [Laravel 11 was released](https://blog.laravel.com/laravel-11-now-available). And with it arrived a new tool in the Laravel ecosystem: [Laravel Reverb](https://reverb.laravel.com/).

Reverb is a separate open-source package that's a first-party WebSocket server for Laravel applications. It helps facilitate real-time communication between client and server.

Before this new package, Laravel had event broadcasting, but basically it didn't have a built-in way to set up a self-hosted WebSocket server. Fortunately, Reverb now gives us that option.

Laravel Reverb has a few key features: it's written in PHP, i's fast, and it;s scalable. It was developed in particular to be horizontally scalable.

Reverb basically allows you to run an application on a single server - but if the application starts to outgrow that server, you can add multiple additional servers. Then those servers can all communicate with each other to distribute the messages between themselves.

## Installation
