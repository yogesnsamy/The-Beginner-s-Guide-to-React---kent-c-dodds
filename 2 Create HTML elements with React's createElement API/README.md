Create HTML elements with React's createElement API: 3:24

Creating elements in HTML - the conventional way:

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Document</title>
  </head>
  <body>
    <div id="root"></div>

    <script type="text/javascript">
      const rootElement = document.getElementById('root');
      const element = document.createElement('div');
      element.textContent = 'hello world';
      element.className = 'container';
      rootElement.appendChild(element);
    </script>

  </body>
</html>

Wt react is similar - use render instead of appendChild
need to link to react global and react dom global below div#id
update code - instead of doc.createelem, use react.createelement, append classname and textContent as obj parm inside react.createElement {className: 'container'}, 'hellow world', 'goodbye world')
instead of using rootElement.appendChild, use ReactDOM.render(element, rootElement)
console.log(element) to see its properties

- has props - with children: 'hello world', className: 'container'
  instead of react.createElement {className: 'container'}, 'hellow world', 'goodbye world'), we can do react.createElement {className: 'container', children: ['hellow world', 'goodbye world']) and it gives the same result
  React.createElement API is simple as element + obj that has all the props we want applied
