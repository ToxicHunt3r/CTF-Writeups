My Writeup:
First, we open the website http://18.184.219.56:8080/
then we get this message "You are not coming from "http://flagland.internal/". "
start BurpSuite intercept the request  send it to the repeater and add this header -> Referer: http://flagland.internal/
then we get another message "Unspecified "secret"."
we change the URL to http://18.184.219.56:8080/?secret=
the page changed to "Incorrect secret"
if we inspected the page content we found a hint
`<!-- hint: secret is ____ which is the name of the protocol that both this server and your browser agrees on... -->`
we change the URL again to `http://18.184.219.56:8080/?secret=http`
we get this message "Sorry we don't have "GET" here but we might have other things like "FLAG"."
change the GET Method to FLAG and Vola we got the Flag: MAPNA{533m5-l1k3-y0u-kn0w-h77p-1836a2f}
