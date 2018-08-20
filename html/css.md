# CSS常用Tips
## display的三个常用属性值：inline, block和inline-block
* inline

  1. 使元素变成行内元素，拥有行内元素的特性，即可以与其它行内元素共享一行，不会独占一行。
  2. 不能更改元素的height和width，大小由实际内容决定。
  3. 可以使用padding、margin的left和right属性，但不能使用top和bottom
* block

  1. 使元素变成块级元素，独占一行，在不设置宽度的情况下，会默认填满父级元素的宽度。即使设置了很小的宽度，也仍然独占一行。
  2. 能够改变元素的height和width
  3. 可以设置padding、margin的各个属性值。
* inline-block

  1. 结合了inline的第一个特点和block的第2、3个特点。
  2. inline-block有个缺点是当两个元素处于同一行时，他们中间会产生4个像素的间隙。这是因为我们在编写代码时两个元素间用了回车符，回车符就相当于空白符。所以我们可以通过对这两个元素的父元素设置font-size为0来消除间隙。

block元素主要有address，blockquote，center，dir，div，dl，fieldset，form，h1，h2，h3，h4，h5，h6，hr，isindex，menu，noframes，noscript，ol，p，pre，table，ul，li。

inline元素主要有a，abbr，acronym，b，bdo，big，br，cite，code，dfn，em，font，i，img，input，kbd，label，q，s，samp，select，small，span，strike，strong，sub，sup，textarea，tt，u，var。

可变元素(根据上下文关系确定该元素是block元素还是inline元素)主要有applet，button，del，iframe，ins，map，object，script。

## 为什么margin-left:auto可以使元素靠右对齐
根据[w3c的规定](https://www.w3.org/html/ig/zh/wiki/CSS2/visudet#blockwidth)，常规流中的块级非置换元素需要满足：margin-left + border-left-width + padding-left + width + padding-right + border-right-width + margin-right = 包含块的宽度。如果margin-left为auto，width非0，其它值都为0，那么margin-left就等于包含块的宽度-自身宽度，所以元素就会靠在包含块的右边位置。