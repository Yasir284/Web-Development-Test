# Question: Explain all the CSS positions(static, fixed, sticky, relative, absolute) with one code example each

## Static:

- The static position is the default position of an element. The element with static position has normal document flow.
- It doesn't get affected with the left, right, top and bottom properties.

**Example:**

```
<style>
  .box {
    position: static;
    width: 200px;
    height: 200px;
    background-color: red;
  }
</style>

<div class="box">Static Position</div>

```

---

## Fixed:

- Element with fixed position gets removed from the normal flow of the document and get fixed at perticular postion in the view port.
- The position of element with fixed position can be changed using properties like left, right, top and bottom.

**Example:**

```
<!-- This element is fixed at position of top 50px and left 50px from the viewport -->

<style>
  .box {
    position: fixed;
    top: 50px;
    left: 50px;
    width: 200px;
    height: 200px;
    background-color: blue;
  }
</style>

<div class="box">Fixed Position</div>

```

---

## Sticky:

- The elements with position sticky will behave like **positioin: relative** until it doesn't touch a particular threshold in the viewport, but after that it behaves like **position: fixed**

**Example:**

```
<!-- This element will get fixed when it comes at top 50px in the viewport -->

<style>
  .box {
    position: sticky;
    top: 50px;
    width: 200px;
    height: 200px;
    background-color: green;
  }
</style>

<div class="box">Sticky Position</div>

```

---

## Relative:

- The element with position relative will be removed from the normal flow of the document and it's position will be relative to it's normal / orignal position.

**Example:**

```
<!-- This element will be 50px left and 50px top from it's orignal position -->

<style>
  .box {
    position: relative;
    left: 50px;
    top: 50px;
    width: 200px;
    height: 200px;
    background-color: orange;
  }
</style>

<div class="box">Relative Position</div>

```

---

## Absolute:

- The element with position absolute will be relative to it's ancestor. Let us understand with the example.

- In the example given below, the **div** tag with the position absolute will be positioned relative to the **html** or **body** tag, depending on the overall structure of the HTML document.

```
<style>
  .box {
    position: absolute;
    left: 50px;
    top: 50px;
    width: 200px;
    height: 200px;
    background-color: orange;
  }
</style>

<div class="box">Absolute Position</div>
```

- Now as we know the element with position relative is removed from the normal flow of the document. So if any ancestor of element with absolute position contain position relative then it will be relative to that element.

**Example**

```
<!-- Here the element with box class will be relative to element will container class -->

<style>
  .container {
    position: relative;
    width: 400px;
    height: 400px;
    background-color: lightgray;
  }

  .box {
    position: absolute;
    top: 50px;
    left: 50px;
    width: 200px;
    height: 200px;
  }


<div class="container">
<div class="box">Absolute Position</div>
</div>

```

---
