# paper-search-input

input search and voice commands

### Use

import:

```sh
<link rel="import" href="/bower_components/paper-search-input/paper-search-input.html">
```

html

```sh
<paper-search-input id="paper-search-input" languaje="es-CO"></paper-search-input>
```

### Config commands
```sh
var paperInputSearch = document.getElementById('paper-search-input');
      paperInputSearch._commandsVoice(
        {
          'hola': function() { alert('Hello world!'); annyang.abort(); },
          'busca a *val':function(val) {
            alert('Buscando a:'+ val);

            paperInputSearch.hearVoiceStop();
          },
          'cuanto es :val + :val2':function(val, val2) {
            var v1 = parseInt(val);
            var v2 = parseInt(val2);

            paperInputSearch.value = 'cuanto es '+v1+' + '+v2;
            alert('el resultado es:'+ (v1 + v2) );

            paperInputSearch.hearVoiceStop();
          }
        }
      );
```

![alt tag](http://imgur.com/5y3Kgih)


![alt tag](http://imgur.com/uqgxdHN)


Use search history option

```sh
<paper-search-input id="paper-search-input" languaje="es-CO" search-history></paper-search-input>
```

add items searchHistory
```sh
var paperInputSearch = document.getElementById('paper-search-input');

paperInputSearch.searchItems = [
  {
    "title":'Historial',
    "subtitle":'',
    "value":'',
    "icon":'history'
  },
  {
    "title":'Clientes enero',
    "subtitle":'ene, 19 2016',
    "value":'2015-01-19',
    "icon":'chevron-right'
  }
];
```
![alt tag](http://imgur.com/ROfSqaN)


License
----

MIT


**Free Component, Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [@thomasfuchs]: <http://twitter.com/thomasfuchs>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [marked]: <https://github.com/chjj/marked>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [keymaster.js]: <https://github.com/madrobby/keymaster>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]:  <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
