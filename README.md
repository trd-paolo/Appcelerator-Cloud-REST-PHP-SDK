# Appcelerator-Cloud-REST-SDK


A Helper Class which will allow you to access ACS, easily using REST and PHP


Instantiating Cloud Class
```php

	include "Cloud.class.php";

	$ACS = new Cloud(array(
			"key" 	=> "fgdr345w234ewds2df3453tedfdsdasd32e"
	));
	// Login using an admin user
	$ACS->login("admin@example.com","123456");
```

Using the Cloud#api() method


example:
```php
	$ACS->api("/push_notification/notify", "POST", array(
  		"channel" => "free_channel", 
  		"payload" => stripcslashes(json_encode((object)array("badge"=>"+1","alert"=>"WisdomSky3"))),
  		"to_ids"  => "everyone"
	));
```