# Tutorial- emastic #




## Instalation ##
Put the following css files into your page:
```
 <link  href="css/reset.css" rel="stylesheet" type="text/css">
 <link  href="css/grid.css" rel="stylesheet" type="text/css">
 <link  href="css/type.css" rel="stylesheet"  type="text/css">
 <!--[if IE]><link  href="css/ie.css" type="text/css" rel="stylesheet"><![endif]-->

```

## CSS Files ##

  * reset.css - based on Eric Meyer [reset.css](http://meyerweb.com/eric/tools/css/reset/)
  * grid.css - the core CSS (building all the grids)
  * type.css - basic css formatting
  * ie.css - resolve some IE bugs
  * gadgets.css (new) - plugin

## How emastic works? ##

The grid sistem is based on ems [elastic layout](http://jontangerine.com/log/2007/09/the-incredible-em-and-elastic-layouts-with-css).

The grid sistem is not limited only on ems. You can use px or % for the page width.
(e.g: width:xx em or width:xx px or width:xx %).

The grid is made from blocks from 5em to 75em.
If the body tag font-size is 100% (1em = 16px).
If the body tag font-size is 75% (1em = 12px). This is default!

Take a look at the [spreadsheet](http://spreadsheets.google.com/pub?key=pXCrVPXw4_XgzS0v_bgZecQ).

I added blocks of 1 and 2 ems for fine tuning.

There is also one block widh 100% and one for fluid columns.  The block can be floated **left** or **right**. And that is it!

## legend ##
All css classes have min. names in order to preserve space.

  * dl - div left
  * dr - div right
  * ml - margin left
  * mr - margin right
  * hp - hundred percent

(e.g dl20 = div floated left, with width of 20em(240px)

## Some code ##
The basic container is "main" class, by default is 70em(840px).

Inside the main container we can put 1,2,3,4 or more columns.

If we need 3 columns we can do:

  * 20em + 20em + 30em = 70em or

  * 10em + 30em + 30em = 70em or

  * 50em + 10em + 10em = 70em ...

```
<div class="main">

 <div class="dl20"> 20 em </div>
 <div class="dl20"> 20 em </div>
 <div class="dl30"> 30 em </div>

 <br class="clear" />
 
 <div class="dl10"> 10 em </div>
 <div class="dl30"> 30 em </div>
 <div class="dl30"> 30 em </div>

 <br class="clear" />

 <div class="dl50"> 50 em </div>
 <div class="dl10"> 10 em </div>
 <div class="dl10"> 10 em </div>

 <br class="clear" />

</div>
```

What if the main container is 80%?

Then we use fluid columns. If we need 3 columns layout we will use 1 fluid and 2 fixed columns.

```
<div class="main">

 <div class="dl20"> 20 em </div>
 <div class="dr20"> 20 em </div>
 <div class="fluid"> fluid </div>

 <br class="clear" />

</div>
```

Just use them like lego blocks!

You can also use Div **inside** Div.

```
<div class="main">

 <div class="dl20"> 20 em
 
   <div class="dl10"> 10 em </div>
   <div class="dl10"> 10 em </div>

 </div>
 
</div>
```

OR:

```
<div class="main">

 <div class="dl20"> 20 em
 
   <div class="dl20"> 20 em (The structure won't break) </div>
   
 </div>
 
</div>
```