# Happy Code-y Things Go Here

I love code reflection. <br />

Why? <br />

Reflection allows you to modify and inspect objects at runtime. <br />

A year ago, I discovered reflection during my internship. Though, I don't remember how I came across reflection. (It may have been because I was playing around with ILSpy at the time.) One of my coworkers was painstakingly trying to hardcode several pages worth of field names to their respective values, but I replaced it with a few lines of code.
The best part was, when the objects were renamed or altered, our code did not need to be changed. It could grab all the field names from the object, and then use those for headers of a datagrid, and then fill the values in for all the objects in the list. 

Brilliant. <br />

Today I found out that JavaScript also utilizes reflection &hearts; <br />

Here I was, staring at a large JSON file and feeling disgusted at the idea of mapping out each property one by one to a list of objects, when, I remembered reflection. <br />

Oh reflection, you wonderful thing, you.

```javascript
  response.data.items.forEach(function (i) {
       var node = {id:i.id,title:i.title};
       i.subitems.forEach(function(property) {
           node[property] = i.subitems[property]; 
       })
     });
```

Magic.
