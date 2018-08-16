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

`<div>`的默认属性就是block，`<a>`和`<span>`的默认属性就是inline。