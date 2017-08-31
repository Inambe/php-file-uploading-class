# PHP File Uploading Class

validate and upload files on server more easily using PHP.

## Getting Started

All you need to get started with this class is, include or autoload this class in you project or file

## Simple uploading

we can start using this class using this simple code.

```
$a = new Upload("input_field_name","directory_to_upload/");
$a->do_upload();
```

## Maximum file size validation

we can add maximum file size(Megabytes) parameter in order to validate file size. [ default=5MB ]

```
$a = new Upload("input_field_name","directory_to_upload/",10);
```

and repeat

```
$a->do_upload();
```

## File extension validation 

we can pass an array of allowed extensions to validate file extension. [ default = ["jpg","png","gif"] ]

```
$a = new Upload("input_field_name","directory_to_upload/",10,["png","jpg"]);
```
## Checking for errors and warnings

we can use `errors()` method to get array of errors and warnings.
Remember `do_upload()` will return false if there will be any error or warning. 

```
$a = new Upload("input_field_name","directory_to_upload/",10,["png","jpg"]);
if($a->do_upload()){
  $a->file_name(); // will return file name
  $a->file_url(); // will return file url(current) 
  // file is uploaded do whatever you want to do
}else{
  var_dump($a->errors());
}
```

## Authors

* **Inambe** - *Developer* - [Inambe](https://facebook.com/inambe.io)
* **kamaltech** *Created for* [Kamaltech](http://kamaltech.io)
