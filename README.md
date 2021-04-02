# Button-switches-with-checkbox-and-css3-fancies
....html.....
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>repl.it</title>
    <link href="style.css" rel="stylesheet" type="text/css" />
  </head>
  <body>
    <div class="switch">
	<input type="checkbox">
	<label></label>
</div> 
  </body>
</html>
.....css.....
.switch {
    width: 50px;
    height: 100px;
    position: centre;
}
.switch label {
    display: block;
    width: 100%;
    height: 100%;
    position: centre;
    background: #dad1b8;
    border-radius: 5px;
    box-shadow:
        inset 0 1px 0 rgb(212, 6, 6),
        0 0 0 1px rgba(199, 202, 15, 0.445),
        0 0 5px 1px rgba(241, 5, 5, 0.479),
        0 2px 0 rgba(54, 201, 10, 0.89),
        inset 0 10px 1px #08b1e44f,
        inset 0 11px 0 rgba(187, 6, 6, 0.788),
        inset 0 -45px 3px rgba(198, 241, 7, 0.116);
}
.switch label:after {
    content: "";
    position: absolute;
    z-index: -1;
    top: -20px;
    left: -25px;
    bottom: -20px;
    right: -25px;
    background: #ccc; /* Fallback */
    background: linear-gradient(#ddd, #bbb);
    border-radius: inherit;
    border: 1px solid #bbb;
    box-shadow:
        0 0 5px 1px rgba(0,0,0,0.15),
        0 3px 3px rgba(0,0,0,0.3),
        inset 0 1px 0 rgba(255,255,255,0.5);
}
.switch label:before {
    content: "";
    position: absolute;
    width: 8px;
    height: 8px;
    top: -13px;
    left: 20px;
    background: #666;
    border-radius: 50%;
    box-shadow:
        0 1px 0 white, /* Subtle reflection on the bottom of the hole */
        0 120px 0 #666, /* Faking a second screw hole... */
        0 121px 0 white; /* And its reflection */
}
.switch input:checked ~ label { /* Button */
    background: #d2cbc3;
    box-shadow:
        inset 0 1px 0 white,
        0 0 0 1px #999,
        0 0 5px 1px rgba(0,0,0,0.2),
        inset 0 -10px 0 #aaa,
        0 2px 0 rgba(255,255,255,0.1),
        inset 0 45px 3px #e0e0E0,
        0 8px 6px rgba(0,0,0,0.18);
}
