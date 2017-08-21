# awesome-jstree
jsTree is jquery plugin, that provides interactive trees. It is absolutely free, open source and distributed under the MIT license.

jsTree is easily extendable, themable and configurable, it supports HTML & JSON data sources, AJAX & async callback loading.

jsTree functions properly in either box-model (content-box or border-box), can be loaded as an AMD module, and has a built in mobile theme for responsive design, that can easily be customized. It uses jQuery's event system, so binding callbacks on various events in the tree is familiar and easy.

How to Start jstree,what are external links needs to be add.
# To get started you need 3 things in your page:

         <script src="//cdnjs.cloudflare.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>

        <link rel="stylesheet" href="//cdnjs.cloudflare.com/ajax/libs/jstree/3.3.3/themes/default/style.min.css" />

        <script src="//cdnjs.cloudflare.com/ajax/libs/jstree/3.3.3/jstree.min.js"></script>

# Populating a tree using HTML

Now we are all set to create a tree, inline HTML is the easiest option (suitable for menus). All you need to do is select a node (using a jQuery selector) and invoke the .jstree() function to let jstree know you want to render a tree inside the selected node. $.jstree.create(element) can be used too.

        <div id="container">
          <ul>
            <li>ESSPL
              <ul>
                <li>Bhubaneswar</li>
                <li>Canada</li>
                <li>Kolkata</li>
              </ul>
            </li>
          </ul>
        </div>

            <script>
            $(function() {
              $('#container').jstree();
            });
            </script>

<a href="https://jsfiddle.net/binaynayak/5rm8pa8b/1/">Demo in Fiddle</a>

# Populating a tree using an array (or JSON)

 Building trees from HTML is easy, but it is not very flexible, inline JS data is a better option:

                      <div id="container"></div>
                      $('#container').jstree({
                      'core' : {
                          'data' : [
                              { "text" : "ESSPL", "children" : [
                                  { "text" : "Bhubaneswar" },
                                  { "text" : "Canada" },
                                  { "text" : "Kolkata" }
                              ]
                              },
                          ]
                      }
                  });



<a href="https://jsfiddle.net/bnkumar58/ck30jt7z/">Demo in Fiddle</a>

Unlike the previous simple HTML example, this time the .jstree() function accepts a config object.

For now it is important to note that jstree will try to parse any data you specify in the core.data key and use it to create a tree. As seen in the previous example, if this key is missing jstree will try to parse the inline HTML of the container.

