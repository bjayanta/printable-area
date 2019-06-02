# Printable Area Functionality 
It's a simple test.

## Using Javascript:
```javascript
function printable(area) {
	var printContents = document.querySelector(area).innerHTML, // get printable content 
		originalContents = document.body.innerHTML; // get document content
	
	// make a temporary document for printable content
	document.body.innerHTML = printContents;
	window.print(); // print the current document

	// restore the original document 
	document.body.innerHTML = originalContents;
}
```

## Using HTML
You can call via 'DOM':
```html
<article>
    <h3>Printable area</h3>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
</article>
    
<button onclick="printable('article')"> Print </button>
```

You can call via 'class':
```html
<article class="article">
    <h3>Printable area</h3>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
</article>
    
<button onclick="printable('.article')"> Print </button> or
<button onclick="printable('article.article')"> Print </button>
```

You can call via 'ID':
```html
<article id="article">
    <h3>Printable area</h3>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
</article>
    
<button onclick="printable('#article')"> Print </button> or
<button onclick="printable('article#article')"> Print </button>
```

Thanks.
