<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AnalogClock</title>
    <style>
        .clock {
            text-align: center;
            height: 500px;
            width: 500px;
            border: 1px solid black;
            border-radius: 50%;
            margin: 100px 450px;
            position: relative;
            background-color: rgb(223, 223, 247);
            font-size: 40px;

            .point {
                color: black;
                text-align: center;
                margin-top: 227px;
                height: 20px;
                width: 20px;
                border-radius: 50%;
                border: 1px solid black;
                background-color: black;
                margin-left: 252px;
            }
        }

        body {
            background-color: rgb(16, 8, 3);
        }

        #secs {
            position: absolute;
            top: 200px;
            left: 720px;
            transform-origin: bottom;
        }

        #mins {
            position: absolute;
            top: 160px;
            left: 720px;
            width: 4px;
            transform-origin: bottom;
        }

        #hrs {
            position: absolute;
            top: 200px;
            left: 720px;
            width: 6px;
            transform-origin: bottom;
        }

        #one {
            position: absolute;
            right: 120px;
            top: 40px;
        }

        #two {
            position: absolute;
            right: 40px;
            top: 120px;
        }

        #three {
            position: absolute;
            right: 10px;
            bottom: 240px;
        }

        #four {
            position: absolute;
            right: 40px;
            bottom: 130px;
        }

        #five {
            position: absolute;
            right: 120px;
            bottom: 40px;
        }

        #six {
            position: absolute;
            left: 250px;
            bottom: 10px;
        }

        #seven {
            position: absolute;
            left: 120px;
            bottom: 40px;
        }

        #eight {
            position: absolute;
            left: 40px;
            bottom: 130px;
        }

        #nine {
            position: absolute;
            left: 10px;
            bottom: 240px;
        }

        #ten {
            position: absolute;
            left: 40px;
            top: 120px;
        }

        #eleven {
            position: absolute;
            left: 120px;
            top: 40px;
        }

        #twelve {
            position: absolute;
            left: 240px;
            top: 10px;
        }

        .hand div {
            position: absolute;
            width: 3px;
            height: var(--h);
            background-color: var(--clr);
            border-radius: 5px;
        }
    </style>
</head>

<body>
    <div class="clock">
        <div class="time" id="one"><b>1</b></div>
        <div class="time" id="two"><b>2</b></div>
        <div class="time" id="three"><b>3</b></div>
        <div class="time" id="four"><b>4</b></div>
        <div class="time" id="five"><b>5</b></div>
        <div class="time" id="six"><b>6</b></div>
        <div class="time" id="seven"><b>7</b></div>
        <div class="time" id="eight"><b>8</b></div>
        <div class="time" id="nine"><b>9</b></div>
        <div class="time" id="ten"><b>10</b></div>
        <div class="time" id="eleven"><b>11</b></div>
        <div class="time" id="twelve"><b>12</b></div>
        <div class="point"></div>
    </div>
    <div class="hand">
        <div id="hrs" style="--h:140px; --clr:rgb(7, 76, 114);"></div>
        <div id="mins" style="--h:180px; --clr: red"></div>
        <div id="secs" style="--h:140px; --clr:#09e03f;"></div>
    </div>
</body>

<script>
    setInterval(() => {
        var date = new Date();
        var rh = date.getHours();
        var rm = date.getMinutes();
        var rs = date.getSeconds();
        document.getElementById("secs").style.transform = `rotate(${6 * rs}deg)`;
        document.getElementById("mins").style.transform = `rotate(${6 * rm}deg)`;
        document.getElementById("hrs").style.transform = `rotate(${30 * rh + rm / 2}deg)`;
    }, 1000)
</script>

</html>
