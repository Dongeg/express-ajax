# express-ajax
```js
$('button').on('click', function(event) {
	event.preventDefault();
	/* Act on the event */
	$.ajax({
		url: '/ajax/test',
		type: 'get',
		dataType: 'json',
		success:function(data){
			$('div').html(data.tips);
		},
		error:function(data){
			alert('error');
		}
	});

});
后端就这么写:
app.get('/ajax/test',function(req,res){
  var ajaxTest={
    tips:"you are not alone"
  };
  res.send(ajaxTest);
});


```
