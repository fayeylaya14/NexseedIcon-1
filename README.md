# HOW TO CREATE SEED KUN USING HTML AND CSS:

**1. Create first the circle/main body of the icon:**

HTML:

`<div class="cont"></div>`

CSS:

```
.cont {
    position: relative;
    width: 190px;
    height: 190px;
    padding: 20px;
}
```

**2. Create the leaves or antenna of Seed Kun:**

HTML

```
<div class="antenna">
  <div class="moon"></div>
</div>
```

*Inside, there is a moon class. This class will be the main antennas. The antenna class serves as
the container.*

CSS:

```
  .antenna {
    display: inline-block;
    position: absolute;
    top: -44px;
    z-index: 1;
    left: 0;
}

.moon {
    position: relative;
    display: block;
    margin: 2rem;
    width: 40px;
    height: 40px;
    background-color: transparent;
    box-shadow: inset 12px 5px 0 3px #15B165;
    border-radius: 50%;
}

.moon::after {
    content: '';
    position: absolute;
    top: -18px;
    right: -34px;
    display: block;
    margin: 2rem;
    width: 25px;
    height: 25px;
    background-color: transparent;
    box-shadow: inset 6px 5px 0 3px #15B165;
    border-radius: 50%;
    transform: rotate(22deg);
}

```

**3. We'll form the circle and the blue crescent-like shape inside the circle**

HTML:

```
<div id="box">
 // insert other divs here
</div>

```
CSS

```
#box {
    width:150px;
    height:150px;
    border-radius:50%;
    border:5px solid #353332;
    background:
      radial-gradient(circle at top left,transparent 59.4%,#353332 60% calc(60% + 4px),#1CAEE3 calc(60% + 5px));
      transform: rotate(19deg);
}
```

**4. For the eyes**

HTML
```
<div id="box">
   <div class="eyes-cont">
       <span class="eyes left"></span>
       <span class="eyes right"></span>
   </div>
</div>
```

CSS:
```
.eyes-cont {
    display: inline-block;
    position: absolute;
    right: 0;
    left: 16px;
    top: -3px;
}
.eyes {
    display: inline-block;
    width: 10px;
    height: 13px;
    border: 3px solid #4FBFF1;
    border-radius: 50%;
    margin-right: 18px;
    margin-top: 50px;
    margin-bottom: -3px;
    transform: rotate(-8deg);
}

.eyes.left {
    border-radius: 34px / 37px;
    height: 12px;
    width: 7px;
}

.eyes.right {
    margin-bottom: 17px;
}
```

**5. For the necktie**
*We have to create separate divs since there are a lot of shapes involved. We first create the outer shapes for the borders then 
the inner shapes. We will be using pseudo elements in this part.*

HTML:
```
<div id="box">
   <div class="eyes-cont">
      <span class="eyes left"></span>
      <span class="eyes right"></span>
    </div>
    <div class="neck-tie">
        <div class="upper"></div>
        <div class="lower">
            <span class="lower-border"></span>
        </div>
    </div>
</div>
```

CSS:
```
.neck-tie  {
  margin: 117px 89px;
  transform: rotate(-45deg);
}

  .lower {
    width: 0;
    height: 0;
    border-bottom: 20px solid #353332;
    border-right: 12px solid transparent;
    transform: rotate(36deg);
    position: relative;
    left: 10px;
    top: -2px;
}

  .lower::before {
    content: '';
    position: absolute;
    width: 0;
    height: 0;
    border-bottom: 20px solid #353332;
    border-right: 13px solid transparent;
    transform: scaleX(-1) rotate(63deg);
    left: -1px;
  }


  .upper {
    width: 0;
    height: 0;
    border-left: 18px solid transparent;
    border-right: 18px solid transparent;
    border-bottom: 21px solid #353332;
    transform: rotate(184deg);
    position: relative;
  }

  .upper::before {
    content: '';
    position: absolute;
    width: 0;
    height: 0;
    border-left: 13px solid transparent;
    border-right: 13px solid transparent;
    border-bottom: 14px solid #EEE328;
    transform: rotate(0deg);
    top: 4px;
    bottom: 9px;
    left: -13px;
  }

  .lower-border {
    display: block;
    width: 0;
    height: 0;
    border-bottom: 16px solid #EEE328;
    border-right: 9px solid transparent;
    transform: rotate(-3deg);
    position: absolute;
    left: 2px;
    top: 2px;
  }

.lower-border:before {
    content: '';
    position: absolute;
    width: 0;
    height: 0;
    border-bottom: 16px solid #EEE328;
    border-right: 9px solid transparent;
    transform: scaleX(-1) rotate(59deg);
    left: -1px;
  }
```
