# awesome-jstree
jsTree is jquery plugin, that provides interactive trees. It is absolutely free, open source and distributed under the MIT license.

jsTree is easily extendable, themable and configurable, it supports HTML & JSON data sources, AJAX & async callback loading.

jsTree functions properly in either box-model (content-box or border-box), can be loaded as an AMD module, and has a built in mobile theme for responsive design, that can easily be customized. It uses jQuery's event system, so binding callbacks on various events in the tree is familiar and easy.

How to Start jstree,what are external links needs to be add.
# To get started you need 3 things in your page:

    jQuery (anything above 1.9.1 will work)
    A jstree theme (there is only one theme supplied by default)
    The jstree source file

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
