# flaxe#Use in html head or npm install flaxe

> <script src="https://unpkg.com/flaxe@1.0.2"></script>

# You only need 
## In HTML code
1.- Define "id" name in the container general element
2.- Define class identifiers on general container children
3.- Call the script flaxe below everything, or use and script directly, but always below

You need class identifiers defined as: "header", "section", "aside", "footer" for view changes specified in the configuration flex box

<pre>
<div id="root">
	<div class="children header">
	</div>
	<div class="children section">
	</div>
	<div class="children aside">
	</div>
	<div class="children footer">
	</div>
	<div class="children other">
	</div>
	<div class="children other">
	</div>
</div>
</pre>

> The elements named "other" will be shown as specified but always below the fundamental structure "section" - "aside" or vice versa

## In the javascript code

1.- Import the script
2.- Create a new Instance
3.- Define the Responsive method and assign it the required parameters: container name, common name of child elements, configuration of flexbox using an object and the order of elements

<pre>
let config = {
	header: "1 1 auto",
	section : "1 0",
	aside : "2 0",
	footer : "1 1 auto",
	other : "2 0 25%" //40% it's fine 
}
const web = new flaxe()
web.Responsive("root", "children",config, [6,2,3,4,5,1])
</pre>

> The "Responsive" method require 4 parameters: general container identifier, class identifiers of the children, the configuration flexbox in an object js, and an array with the order of the elements 
