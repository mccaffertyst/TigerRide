# TigerRide
COSC 412 Term Project 

/*
To change this license header, choose License Headers in Project Properties.
To change this template file, choose Tools | Templates
and open the template in the editor.
*/
/* 
    Created on : Mar 27, 2018, 12:47:27 PM
    Author     : jordanpuglisi
*/

body{
    background-image: linear-gradient(rgba(0,0,0,0.6),rgba(0,0,0,0.6)),
        url(login_background.jpg);
    height: 100vh;
    background-size: cover;
    background-position: center;
}

.login-page{
    width: 360px;
    padding: 10% 0 0;
    margin: auto;
}

.form{
    position: relative;
    z-index: 1;
    background: #FFFFFF;
    max-width: 360px;
    margin: 0 auto 100px;
    padding: 45px;
    text-align: center;
}

.form input{
    font-family: "Roboto", sans-serif;
    outline: 1;
    background: #F2F2F2;
    width: 100%;
    border: 0;
    margin: 0 0 15px;
    padding: 15px;
    box-sizing: border-box;
    font-size: 14px;   
}

.form button{
    font-family: "Roboto", sans-serif;
    text-transform: uppercase;
    outline: 0;
    background: #4CAF50;
    width: 100%;
    border: 0;
    padding: 15px;
    color: #FFFFFF;
    font-size: 14px;
    cursor: pointer;
}

.form button:hover,.form button:active{
    background: #43A047
}

.form .message{
    margin: 15px 0 0;
    color: crimson;
    font-size: 12px;
}

.form .message a{
    color: #4CAF50;
    text-decoration: none;
}

.form .register-form{
    display: none
}
