var nowplzstop = false;
var totalProf = 0;
var nextbet = 0;
var autobase = true
var boost=false
var boostnum=5
_channel = "https://t.me/unusedspace";
$(" <link href=\"https://netdna.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css\" rel=\"stylesheet\"> <link href=\"https://fonts.googleapis.com/css?family=Electrolize\" rel=\"stylesheet\"> <div id=\"bot\" class=\"popup show normal\" style=\"position: fixed; top: 0px;\"> <div class=\"bot-container\"> <div class=\"popup-body\" style=\"max-height: 350px;\"> <div class=\"mCustomScrollBox mCS-sidebar mCSB_vertical mCSB_outside\" style=\"max-height: none;\" tabindex=\"0\"> <div class=\"mCSB_container mCS_y_hidden mCS_no_scrollbar_y\" style=\"position:relative; top:0; left:0;\" dir=\"ltr\"> <div class=\"inputBox\"> <center> <font style=\"color: #fff; font-size: 15px;\"> <b style=\"color: gold; font-size: 2em;\">🏆Cy4nPRIVATE v.LG.13.04🏆</b> </font> </center> </div> </div> </div> </div> <div class=\"label center bot-stats-container\"> <div class=\"bot-stats-body\"> <div> <div class=\"game-dice\"> <div class=\"game-box\"> <div class=\"number prediction\"> <span id=\"resultDirection\">O</span> <span class=\"title\">DIRECTION</span> </div> <div class=\"devider\"></div> <div class=\"number result\"> <span id=\"resultNumber\">50</span> <span class=\"title\">PREDICTION</span> </div> </div> </div> <div id=\"chart\" style=\"height: 340px; width: 552px\"></div> <div class=\"relatory\"> <table> <tbody> <tr> <td>STATIC 1</td> <td>STATIC 2</td> </tr> <tr> <td> <div class=\"botTooltip relat\"> <span id=\"bot-game\">" + user.game.toUpperCase() + "</span> <span class=\"botTooltiptext\">GAME</span> </div> </td> <td> <div class=\"botTooltip relat\"> <img src=\"https://luckygames.io/assets/coins/small/" + coin.value + ".png\" id=\"bot-coin\"> <span class=\"botTooltiptext\">COIN</span> </div> </td> </tr> <tr> <td> <div class=\"botTooltip relat\"> <span id=\"bot-time\">00:00:00:00</span> <span class=\"botTooltiptext\">TIME</span> </div> </td> <td> <div class=\"botTooltip relat\"> <span id=\"bot-speed\">0.00</span> <span class=\"botTooltiptext\">SPEED</span> </div> </td> </tr> <tr> <td> <div class=\"botTooltip relat\"> <span id=\"bot-balance\">" + balance.value + "</span> <span class=\"botTooltiptext\">BALANCE</span> </div> </td> <td> <div class=\"botTooltip relat\"> <span id=\"bot-profit\">0.00000000</span> <span class=\"botTooltiptext\">PROFIT</span> </div> </td> </tr> <tr> <td> <div class=\"botTooltip relat\"> <span id=\"bot-wagered\">0.00000000</span> <span class=\"botTooltiptext\">WAGERED</span> </div> </td> <td> <div class=\"botTooltip relat\"> <span id=\"bot-max-bet\">0.00000000</span> <span class=\"botTooltiptext\">MAX BET</span> </div> </td> </tr> <tr> <td> <div class=\"botTooltip relat\"> <span id=\"bot-win-streak\">0</span> <span class=\"botTooltiptext\">WIN STREAK</span> </div> </td> <td> <div class=\"botTooltip relat\"> <span id=\"bot-lose-streak\">0</span> <span class=\"botTooltiptext\">LOSE STREAK</span> </div> </td> </tr> <tr> <td> <div class=\"botTooltip relat\"> <span id=\"bot-max-win-streak\">0</span> <span class=\"botTooltiptext\">MAX WIN STREAK</span> </div> </td> <td> <div class=\"botTooltip relat\"> <span id=\"bot-max-lose-streak\">0</span> <span class=\"botTooltiptext\">MAX LOSE STREAK</span> </div> </td> </tr> </tbody> </table> </div> </div> </div> </div> <div class=\"popup-footer\"> <div class=\"botTooltip\"> <input type=\"text\" id=\"basebetAmount\" value=\"0.00000000\"> <span class=\"botTooltiptext\">Base bet</span> </div> <div class=\"botTooltip\"> <input type=\"text\" id=\"overBalance\" value=\"0.00000000\"> <span class=\"botTooltiptext\">Over balance</span> </div> <div class=\"botTooltip\"> <input type=\"text\" id=\"underBalance\" value=\"0.00000000\"> <span class=\"botTooltiptext\">Under balance</span> </div> <div class=\"func\"> <button id=\"min\" class=\"btn blue\" onclick=\"min();\">DONATE</button> <button id=\"play\" class=\"btn green\">START</button> <button id=\"reset\" class=\"btn navy\" onclick=\"reset();\">RESET</button> <button id=\"showChart\" class=\"btn grey\"><b class=\"fa fa-eye-slash\" style=\"font-size:1.2em\"></b> CHART</button> <button id=\"showStatic\" class=\"btn purple\"><b class=\"fa fa-eye-slash\" style=\"font-size:1.2em\"></b> STATIC</button> </div> </div> </div> </div> <style> #bot { position: fixed; top: 105.5px; width: 600px; height: 560px; } #bot .popup-body { position: relative; overflow: visible; max-height: 376px; } #bot .bot-stats-container { border-top: 1px solid #000; border-radius: 5px; width: 92%; margin-left: 4.3%; margin-bottom: 4%; background: #121212; } b { font-family: 'Electrolize', sans-serif; } #bot .bot-stats-body tbody tr td, #bot .bot-stats-body tbody tr th { font-size: 1.2em; padding-left: 25px; font-family: 'Electrolize', sans-serif; } .bot-stats-body::-webkit-scrollbar { width: 0px; } #bot input { border: none; } #bot span.btn { margin: 0px 5px 0px 5px; padding: 8px; } #bot font { cursor: pointer; } #bot input { margin-left: 2px; height: 40px; background: #131313; border: 1px #222222 solid; font-size: 1.3em; font-family: \"Electrolize\"; color: #ffffff; box-sizing: border-box; text-align: center; word-break: break-word; -webkit-border-radius: 3px; -moz-border-radius: 3px; border-radius: 3px; -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, .8); -moz-box-shadow: inset 0 1px 1px rgba(0, 0, 0, .8); box-shadow: inset 0 1px 1px rgb(156, 145, 145); -webkit-transition: all 0.3s ease-out; -moz-transition: all 0.3s ease-out; -o-transition: all 0.3s ease-out; -ms-transition: all 0.3s ease-out; } #bot .bot-stats-body { height: 340px; overflow-y: scroll; scrollbar-width: none; } #bot .bot-stats { margin-left: 40px; } #sidebar .sidebarNav .tab .icon._BOT { background: url('https://cdn0.iconfinder.com/data/icons/halloween-theme-objects-in-flat-ui-design-style/432/flat.halloween.skull-512.png') 50% no-repeat; background-size: 45px; } #bot #chart { display: none; } #bot #chart canvas { border-radius: 3px; } #bot .func { margin-top: 10px; margin-left: 2px; } #bot .func button { font-family: 'Electrolize', sans-serif; max-width: 108px; margin: 0; } #bot .btn.purple { background: #9B59B6; } #bot .btn.purple:hover { background: #AF7AC5; } #bot .botTooltip { display: initial; width: 100%; } #bot .btn.navy { background:#2C3E50 } #bot .btn.navy:hover { background: #34495E; } .botTooltip { position: relative; display: inline-block; font-family: \"Electrolize\"; } .botTooltip .botTooltiptext { visibility: hidden; width: 120px; background-color: #ffffff; color: #000; text-align: center; border-radius: 3px; padding: 5px 0px; margin: -25px 0px 0px -156.7px; border-bottom: 1px dotted #000; position: absolute; z-index: 100000000; } .botTooltip:hover .botTooltiptext { visibility: visible; } .dice.light .botTooltip .botTooltiptext { background-color: #000; border-bottom: 1px dotted #fff; color: #fff; } #bot .botTooltip.relat .botTooltiptext { margin: -32px 0px 0px -65px; } #bot .bot-stats-body .relatory { top: 0; display: none; } #bot table, #bot td, #bot th { border: 1px solid #111; text-align: center; background: #333; } #bot table { border-collapse: collapse; width: 100%; } #bot th, #bot td { padding: 15px; } #bot .game-dice { position: relative; text-align: center; margin-top: 45px; } #bot .game-dice .game-box { position: relative; display: inline-block; text-align: center; font-size: 130px; height: 220px; font-weight: 600; font-family: \"Segoe UI Bold\"; padding: 0 40px 0; color: #ffffff; background: rgba(0, 0, 0, 0.6); border: 5px solid rgba(0, 0, 0, 0.7); -webkit-border-radius: 10px; -moz-border-radius: 10px; border-radius: 10px; } #bot .game-dice .game-box:after { content: \"\"; position: absolute; bottom: -15px; left: 0; width: 100%; height: 20px; z-index: 0!important; background: rgba(0, 0, 0, .5); box-shadow: 0px 0 15px 10px rgba(0, 0, 0, .5); -webkit-border-radius: 1000px; -moz-border-radius: 1000px; border-radius: 1000px; } #bot .game-dice .game-box .number { width: 150px; text-align: center; display: inline-block; vertical-align: top; } #bot .game-dice .game-box .number input { background: transparent; font-family: \"Segoe UI Bold\"; border: none; font-size: 130px; color: #ffffff; width: 145px; text-align: center; outline: none; padding: 0; margin: 0; } #bot .game-dice .game-box .number.prediction, #bot .game-dice .game-box .number.result { color: #2eab5b; } #bot .game-dice .game-box .number.result.lose { color: #ab2e40; } #bot .game-dice .game-box .devider { position: relative; display: inline-block; width: 5px; height: 100%; margin: 0 36px; background: rgba(0, 0, 0, 0.7); vertical-align: top; } #bot .game-dice .game-box .devider span { position: absolute; font-size: 50px; left: -10px; top: 50%; margin-top: -50px; } #bot .game-dice .game-box span.title { display: block; font-size: 14px; color: #999999; } body.light #bot .game-dice .game-box span.title { color: #676767; } #bot .game-dice .direction { position: absolute; top: 90px; font-size: 32px; cursor: pointer; -webkit-transition: all 0.3s ease-out; -moz-transition: all 0.3s ease-out; -o-transition: all 0.3s ease-out; -ms-transition: all 0.3s ease-out; transition: all 0.3s ease-out; } #bot .game-dice .direction:hover { color: #ffffff; } #bot .game-dice .direction.active { color: #ffffff; border-bottom: 1px #ffffff solid; } </style> ").appendTo("body");
$("<div id=\"BOT\"><div class=\"tab popup-show\"><div class=\"icon _BOT\"></div> BOT </div></div>").appendTo(".sidebarNav");
$("#BOT").on("click", function () {
    if ($("#bot").hasClass("show normal")) {
        $("#bot").removeClass("show normal").addClass("scale");
        $(".popup-bg").fadeOut()
    } else {
        $("#bot").removeClass("scale").addClass("show normal");
        $(".popup-bg").fadeOut()
    }
});

let under = [
    1,
    99.00,
    49.50,
    33.00,
    24.75,
    19.80,
    16.50,
    14.14,
    12.38,
    11.00,
    9.90,
    9.00,
    8.25,
    7.62,
    7.07,
    6.60,
    6.19,
    5.82,
    5.50,
    5.21,
    4.95,
    4.71,
    4.50,
    4.30,
    4.13,
    3.96,
    3.81,
    3.67,
    3.54,
    3.41,
    3.30,
    3.19,
    3.09,
    3.00,
    2.91,
    2.83,
    2.75,
    2.68,
    2.61,
    2.54,
    2.48,
    2.41,
    2.36,
    2.30,
    2.25,
    2.20,
    2.15,
    2.11,
    2.06,
    2.02,
    1.98,
    1.94,
    1.90,
    1.87,
    1.83,
    1.80,
    1.77,
    1.74,
    1.71,
    1.68,
    1.65,
    1.62,
    1.60,
    1.57,
    1.55,
    1.52,
    1.50,
    1.48,
    1.46,
    1.43,
    1.41,
    1.39,
    1.38,
    1.36,
    1.34,
    1.32,
    1.30,
    1.29,
    1.27,
    1.25,
    1.24,
    1.22,
    1.21,
    1.19,
    1.18,
    1.16,
    1.15,
    1.14,
    1.13,
    1.11,
    1.10,
    1.09,
    1.08,
    1.06,
    1.05,
    1.04,
    1.03,
    1.02,
    1.01
]
colors = [
    "#CD5C5C",
    "#F08080",
    "#FA8072",
    "#E9967A",
    "#FFA07A",
    "#DC143C",
    "#FF0000",
    "#B22222",
    "#8B0000",
    "#FFC0CB",
    "#FFB6C1",
    "#FF69B4",
    "#FF1493",
    "#C71585",
    "#DB7093",
    "#FFA07A",
    "#FF7F50",
    "#FF6347",
    "#FF4500",
    "#FF8C00",
    "#FFA500",
    "#FFD700",
    "#FFFF00",
    "#FFFFE0",
    "#FFFACD",
    "#FAFAD2",
    "#FFEFD5",
    "#FFE4B5",
    "#FFDAB9",
    "#EEE8AA",
    "#F0E68C",
    "#BDB76B",
    "#E6E6FA",
    "#D8BFD8",
    "#DDA0DD",
    "#EE82EE",
    "#DA70D6",
    "#FF00FF",
    "#FF00FF",
    "#BA55D3",
    "#9370DB",
    "#8A2BE2",
    "#9400D3",
    "#9932CC",
    "#8B008B",
    "#800080",
    "#4B0082",
    "#6A5ACD",
    "#483D8B",
    "#7B68EE",
    "#ADFF2F",
    "#7FFF00",
    "#7CFC00",
    "#00FF00",
    "#32CD32",
    "#98FB98",
    "#90EE90",
    "#00FA9A",
    "#00FF7F",
    "#3CB371",
    "#2E8B57",
    "#228B22",
    "#008000",
    "#006400",
    "#9ACD32",
    "#6B8E23",
    "#808000",
    "#556B2F",
    "#66CDAA",
    "#8FBC8F",
    "#20B2AA",
    "#008B8B",
    "#008080",
    "#00FFFF",
    "#E0FFFF",
    "#AFEEEE",
    "#7FFFD4",
    "#40E0D0",
    "#48D1CC",
    "#00CED1",
    "#5F9EA0",
    "#4682B4",
    "#B0C4DE",
    "#B0E0E6",
    "#ADD8E6",
    "#87CEEB",
    "#87CEFA",
    "#00BFFF",
    "#1E90FF",
    "#6495ED",
    "#7B68EE",
    "#4169E1",
    "#0000FF",
    "#0000CD",
    "#00008B",
    "#000080",
    "#191970"
]
var objSelecionado = null;
var mouseOffset = null;
function addEvent(_0xb2e6x4, _0xb2e6x5, _0xb2e6x6) {
    if (typeof _0xb2e6x4 == "string") {
        if (null == (_0xb2e6x4 = document.getElementById(_0xb2e6x4))) {
            throw new Error("Elemento HTML não encontrado. Não foi possível adicionar o evento.")
        }
    };
    if (_0xb2e6x4.attachEvent) {
        return _0xb2e6x4.attachEvent(("on" + _0xb2e6x5), _0xb2e6x6)
    } else {
        if (_0xb2e6x4.addEventListener) {
            return _0xb2e6x4.addEventListener(_0xb2e6x5, _0xb2e6x6, true)
        } else {
            throw new Error("Seu browser não suporta adição de eventos. Senta, chora e pega um navegador mais recente.")
        }
    }
}
function mouseCoords(_0xb2e6x8) {
    if (typeof (_0xb2e6x8.pageX) !== "undefined") {
        return {
            x: _0xb2e6x8.pageX,
            y: _0xb2e6x8.pageY
        }
    } else {
        return {
            x: _0xb2e6x8.clientX + document.body.scrollLeft - document.body.clientLeft,
            y: _0xb2e6x8.clientY + document.body.scrollTop - document.body.clientTop
        }
    }
}
function getPosition(_0xb2e6xa, _0xb2e6x8) {
    var _0xb2e6x8 = _0xb2e6x8 || window.event;
    if (_0xb2e6xa.constructor == String) {
        _0xb2e6xa = document.getElementById(_0xb2e6xa)
    };
    var _0xb2e6xb = 0,
        _0xb2e6xc = 0;
    var _0xb2e6xd = mouseCoords(_0xb2e6x8);
    while (_0xb2e6xa.offsetParent) {
        _0xb2e6xb += _0xb2e6xa.offsetLeft;
        _0xb2e6xc += _0xb2e6xa.offsetTop;
        _0xb2e6xa = _0xb2e6xa.offsetParent
    };
    _0xb2e6xb += _0xb2e6xa.offsetLeft;
    _0xb2e6xc += _0xb2e6xa.offsetTop;
    return {
        x: _0xb2e6xd.x - _0xb2e6xb,
        y: _0xb2e6xd.y - _0xb2e6xc
    }
}
function dragdrop(_0xb2e6xf, _0xb2e6x10) {
    _0xb2e6xf = $("#bot .popup-body")[0];
    _0xb2e6x10 = $("#bot")[0];
    _0xb2e6xf.style.cursor = "move";
    if (!_0xb2e6x10.style.position || _0xb2e6x10.style.position == "static") {
        _0xb2e6x10.style.position = "absolute"
    };
    _0xb2e6xf.onmousedown = function (_0xb2e6x8) {
        objSelecionado = _0xb2e6x10;
        mouseOffset = getPosition(objSelecionado, _0xb2e6x8)
    };
    document.onmouseup = function () {
        objSelecionado = null
    };
    document.onmousemove = function (_0xb2e6x8) {
        if (objSelecionado) {
            var _0xb2e6x8 = _0xb2e6x8 || window.event;
            var _0xb2e6x11 = mouseCoords(_0xb2e6x8);
            var _0xb2e6x12 = objSelecionado.parentNode;
            objSelecionado.style.left = (_0xb2e6x11.x - mouseOffset.x - _0xb2e6x12.offsetLeft) + "px";
            objSelecionado.style.top = (_0xb2e6x11.y - mouseOffset.y - _0xb2e6x12.offsetTop) + "px";
            objSelecionado.style.margin = "0px";
            return false
        }
    }
}
dragdrop();
$("#showChart").click(function () {
    if ($(this).hasClass("active")) {
        $(this).removeClass("active");
        $("#showChart b").removeClass("fa-eye").addClass("fa-eye-slash");
        $("#showStatic b").removeClass("fa-eye").addClass("fa-eye-slash");
        $("#bot #chart").fadeOut();
        $("#bot .bot-stats-body .relatory").fadeOut();
        $("#bot .game-dice").fadeIn()
    } else {
        $(this).addClass("active");
        $("#showStatic").removeClass("active");
        $("#showChart b").removeClass("fa-eye-slash").addClass("fa-eye");
        $("#showStatic b").removeClass("fa-eye").addClass("fa-eye-slash");
        $("#bot #chart").fadeIn();
        $("#bot .bot-stats-body .relatory").fadeOut();
        $("#bot .game-dice").fadeOut()
    }
});
$("#showStatic").click(function () {
    if ($(this).hasClass("active")) {
        $(this).removeClass("active");
        $("#showStatic b").removeClass("fa-eye").addClass("fa-eye-slash");
        $("#showChart b").removeClass("fa-eye").addClass("fa-eye-slash");
        $("#bot #chart").fadeOut();
        $("#bot .bot-stats-body .relatory").fadeOut();
        $("#bot .game-dice").fadeIn()
    } else {
        $(this).addClass("active");
        $("#showChart").removeClass("active");
        $("#showStatic b").removeClass("fa-eye-slash").addClass("fa-eye");
        $("#showChart b").removeClass("fa-eye").addClass("fa-eye-slash");
        $("#bot #chart").fadeOut();
        $("#bot .bot-stats-body .relatory").fadeIn();
        $("#bot .game-dice").fadeOut()
    }
});
$("#bot font b").click(function () {
    window.open(_channel)
});
randomizeSeed();
console.clear();
var run = false;
hideChart = true;
hideStatic = true;
sbalance = parseFloat(document.getElementById("balance").value);
basebetAmount = 0;
betAmount = 0;
maxbetAmount = 0;
prediction = Math.floor(90);
direction = "under";
chance = 90;
balance = 0;
overBalance = 0;
underBalance = 0;
bet = 0;
win = 0;
lose = 0;
winStreak = 0;
loseStreak = 0;
maxWinStreak = 0;
maxLoseStreak = 0;
lossAmount = 0;
wagered = 0;
profitWagered = 0;
profit = 0;
profitt = 0;
profittt = 0;
largestProfittt = 0;
largestProfit = 0;
startTime = new Date();
onTime = 0;
playTime = 0;
playDay = 0;
playHour = 0;
playMinute = 0;
playSecond = 0;
speed = 0;
round = 0;
roundd = 0;
seed = 111;
runseed = 0;
changeseed = Math.floor(10);
dsp = [];
chart = "";
color = "";
increasebetEveryLosts = Math.floor(5);
increasebetBy = 2;
co = (1 / prediction) * 99;
cco = co;
lc1 = 0;
lc2 = 0;
sbr = parseFloat(document.getElementById("balance").value);
pp = 0;
negs = 0;
n = Math.floor((Math.random() * (9 - 6 + 1)) + 6);
$.getScript("https://canvasjs.com/assets/script/canvasjs.min.js").done(function (_0xb2e6x14, _0xb2e6x15) {
    dps = [{
        x: 0,
        y: 0
    }];
    chart = new CanvasJS.Chart("chart", {
        backgroundColor: "#ffffff",
        theme: "light1",
        zoomEnabled: true,
        axisX: {
            includeZero: false
        },
        axisY: {
            includeZero: false
        },
        title: {
            fontColor: "green",
            fontSize: 2e1,
            padding: 2e1
        },
        data: [{
            type: "line",
            dataPoints: dps
        }]
    });
    chart.render()
});
function updateChart(_0xb2e6x17, _0xb2e6x18, _0xb2e6x19) {
    dps.push({
        x: _0xb2e6x17,
        y: _0xb2e6x18,
        color: _0xb2e6x19
    });
    if (dps[dps.length - 2]) {
        dps[dps.length - 2].lineColor = _0xb2e6x19
    };
    if (dps.length > 100000) {
        dps.shift()
    };
    chart.render()
}
function min() {
    Chat.easyTip('mrcyjanekdev'); return false;
}
$("#play").on("click", function () {
    run == true ? (play(this, "Start", false, false), $(this).addClass("green").removeClass("red")) : (play(this, "Stop", true, true), $(this).addClass("red").removeClass("green"));
    basebetAmount = parseFloat($("#basebetAmount").val());
    overBalance = parseFloat($("#overBalance").val());
    underBalance = parseFloat($("#underBalance").val());
    betAmount = basebetAmount;
    direction = "under";
    chance = prediction;
    $("#overBalance").val(overBalance.toFixed(8));
    $("#underBalance").val(underBalance.toFixed(8));
    doBet()
});
function play(_0xb2e6xa, _0xb2e6x1c, _0xb2e6x1d) {
    $(_0xb2e6xa).html(_0xb2e6x1c);
    run = _0xb2e6x1d;
    $("#basebetAmount").prop("disabled", _0xb2e6x1d);
    $("#overBalance").prop("disabled", _0xb2e6x1d);
    $("#underBalance").prop("disabled", _0xb2e6x1d);
    $("#min").prop("disabled", _0xb2e6x1d);
    $("#reset").prop("disabled", _0xb2e6x1d)
}
function reset() {
    sbalance = parseFloat(document.getElementById("balance").value);
    basebetAmount = 0;
    betAmount = 0;
    maxbetAmount = 0;
    prediction = Math.floor(90);
    direction = "under";
    chance = 90;
    balance = 0;
    overBalance = 0;
    underBalance = 0;
    bet = 0;
    win = 0;
    lose = 0;
    winStreak = 0;
    loseStreak = 0;
    maxWinStreak = 0;
    maxLoseStreak = 0;
    lossAmount = 0;
    wagered = 0;
    profitWagered = 0;
    profit = 0;
    profitt = 0;
    profittt = 0;
    largestProfittt = 0;
    largestProfit = 0;
    startTime = new Date();
    onTime = 0;
    playTime = 0;
    playDay = 0;
    playHour = 0;
    playMinute = 0;
    playSecond = 0;
    speed = 0;
    round = 0;
    roundd = 0;
    dsp = [];
    chart = "";
    color = "";
    increasebetEveryLosts = Math.floor(5);
    increasebetBy = 2;
    co = (1 / prediction) * 99;
    cco = co;
    lc1 = 0;
    lc2 = 0;
    sbr = parseFloat(document.getElementById("balance").value);
    pp = 0;
    negs = 0;
    n = Math.floor((Math.random() * (9 - 6 + 1)) + 6);
    $.getScript("https://canvasjs.com/assets/script/canvasjs.min.js").done(function (_0xb2e6x14, _0xb2e6x15) {
        dps = [{
            x: 0,
            y: 0
        }];
        chart = new CanvasJS.Chart("chart", {
            backgroundColor: colors[Number(Math.random()*(colors.length-1)).toFixed(0)],
            theme: "light1",
            zoomEnabled: true,
            axisX: {
                includeZero: false
            },
            axisY: {
                includeZero: false
            },
            title: {
                fontColor: colors[Number(Math.random()*(colors.length-1)).toFixed(0)],
                fontSize: 2e1,
                padding: 2e1
            },
            data: [{
                type: "line",
                dataPoints: dps
            }]
        });
        chart.render()
    });
    return
}
function doBet(prediction = 50, betAmount = 0.00000001, direction = 'under', info = 'new') {
    if (run === true) {
        jQuery.ajax({
            url: "https://"+user.domain+"/play/",
            type: "POST",
            dataType: "html",
            timeout: 6e4,
            data: {
                game: "dice",
                coin: $("#coin").val(),
                betAmount: betAmount,
                prediction: prediction,
                direction: direction,
                clientSeed: $("#clientSeed").val(),
                serverSeedHash: $("#serverSeedHash").html(),
                session: getCookie("SESSION"),
                action: "playBet",
                hash: user.hash
            },
            success: function (_0xb2e6x20) {
                var _0xb2e6x20 = JSON.parse(_0xb2e6x20);
                if (_0xb2e6x20.result === true) {
                    bet++;
		    var gameresult = _0xb2e6x20.gameResult;
		    var resultnumber = _0xb2e6x20.resultNumber;
                    onTime = new Date().getTime();
                    playTime = onTime - startTime;
                    playDay = Math.floor(playTime / (1e3 * 6e1 * 6e1 * 24));
                    playHour = Math.floor((playTime % (1e3 * 6e1 * 6e1 * 24)) / (1e3 * 6e1 * 6e1));
                    playMinute = Math.floor((playTime % (1e3 * 6e1 * 6e1)) / (1e3 * 6e1));
                    playSecond = Math.floor((playTime % (1e3 * 6e1)) / 1e3);
                    speed = parseFloat((bet / playTime) * 1000);
                    balance = parseFloat(_0xb2e6x20.balance);
		    $('#balance').animateBalance(_0xb2e6x20.balance);
                    wagered += parseFloat(betAmount);
		    profittt = parseFloat(_0xb2e6x20.profit);
                    profit += parseFloat(_0xb2e6x20.profit);
                    profitWagered = (wagered * 0.1) / 1e2;
                    profitt = 100 * (balance - sbalance) / sbalance;
                    if (profit > largestProfit) {
                        largestProfit = profit
                    };
                    maxbetAmount = Number(maxbetAmount)
                    if (_0xb2e6x20.gameResult === "win") {
                        win++;
                        winStreak++;
                        loseStreak = 0;
                        color = "green"
                    } else {
                        lose++;
                        loseStreak++;
                        winStreak = 0;
                        color = "red"
                    };
                    color = colors[Number(Math.random()*(colors.length-1)).toFixed(0)]
                    if (winStreak >= maxWinStreak) {
                        maxWinStreak = winStreak
                    };
                    if (loseStreak >= maxLoseStreak) {
                        maxLoseStreak = loseStreak
                    };
                    if (betAmount >= maxbetAmount) {
                        maxbetAmount = betAmount
                    };
		    if (profittt > largestProfittt) {
                        largestProfittt = profittt
                    };
                    $("#serverSeedHash").html(_0xb2e6x20.serverSeedHash);
		    $("#bot #resultDirection").text(direction == "under" ? "U" : "O").css({
			"color": gameresult == 'win' ? "#2eab5b" : "#ab2e40"
                    });
		    $("#bot #resultNumber").text(prediction).css({
			"color": gameresult == 'win' ? "#2eab5b" : "#ab2e40"
                    });
                    $("#bot-game").text(user.game.toUpperCase());
                    $("#bot-coin")[0].src = "https://luckygames.io/assets/coins/small/" + $("#coin").val() + ".png";
                    $("#bot-time").text(playDay + ":" + playHour + ":" + playMinute + ":" + playSecond);
                    $("#bot-speed").text(speed.toFixed(2));
                    $("#bot-balance").text(balance.toFixed(8));
                    $("#bot-profit").text(profit.toFixed(8) + " (" + profitt.toFixed(2) + "%)");
                    $("#bot-wagered").text(wagered.toFixed(8));
                    $("#bot-max-bet").text(/*maxbetAmount.toFixed(8)*/'todo');
                    $("#bot-win-streak").text(winStreak);
                    $("#bot-lose-streak").text(loseStreak);
                    $("#bot-max-win-streak").text(maxWinStreak);
                    $("#bot-max-lose-streak").text(maxLoseStreak);
		    $('#betAmount').val(Number(betAmount).toFixed(8));
		    $('#prediction').val(prediction);
		    if (direction === 'under') {
                    	$('#rollUnder').click();
                    } else {
                    	$('#rollOver').click();
                    }
		    $('#resultNumber').html(resultnumber);
		    if (gameresult == 'win') $('#resultNumber').css('color', '#2eab5b');
    					else $('#resultNumber').css('color', '#ab2e40');
		    $('#currentWagered').html(wagered.toFixed(8));
		    $('#currentProfit').html(profit.toFixed(8));
		    if (profit < 0) $('#currentProfit').css('color', '#ab2e40');
    		    	       else $('#currentProfit').css('color', '#2eab5b');
		    $('#currentBets').html(bet);
		    $('#currentWins').html(win);
		    $('#currentLosses').html(lose);
		    $('#currentLuck').html(profitt.toFixed(2));
		    if (profit < 0) $('#currentLuck').css('color', '#ab2e40');
    			       else $('#currentLuck').css('color', '#2eab5b');
		    $('#currentMaxBet').html(/*maxbetAmount.toFixed(8)*/'todo');
		    $('#currentMaxProfit').html(largestProfittt.toFixed(8));
                    updateChart(bet, profit, color);
                    if ((underBalance > balance && underBalance != 0) || (overBalance < balance && overBalance != 0)) {
                        run = false
                    }
                    let a = [5,5,5,5,13,24,35,77,66,75,88,98]
                    console.log(loseStreak.toFixed(0)+" of "+Number(a.length-1));
                    if (nowplzstop == true) {
                        alert("STOP GAMBLING NOW!\n\nSCRIPT ALMOST (or actually) FAILED, TRY AGAIN TOMORROW");
                        window.location.href = "https://pastebin.com/nKGiqZSv";
                    }
                    if (loseStreak.toFixed(0) == Number(a.length-1)) {
                        nowplzstop = true;
                    }
                    if (autobase == true) {
                        let divid = 0;
                        let tpc = 1
                        for (var i = a.length - 1; i >= 0; i--) {
                            if ( i != 0 ) {
                                tpc = (Number((tpc*1)/(Number(under[a[i]])-1))) - 0 + tpc-0
                            }
                        }
                        divid = tpc*1
                        basebetAmount=balance/divid
                    }
                    nextbet = basebetAmount
                    totalProf = totalProf - 0 + ((Number(_0xb2e6x20.profit)) - 0) - 0;
                                        //prediction = 50, betAmount = 0.00000001, direction = 'under', info
                    if (totalProf > 0) {
                        totalProf = 0
                    }
                    if (win) {
                        nextbet = basebetAmount;
                        prediction = 90+(Math.random()*8)
                    }
                    if (lose) {
                        let methodid = a[loseStreak.toFixed(0)]
                        prediction = methodid
                        nextbet = Number((totalProf*-1)/(Number(under[methodid])-1))
                    }
                    if (nextbet < basebetAmount && false) {
                        nextbet = basebetAmount
                    }
                    if ((Math.random()*10).toFixed(0) && lose && boost) {
                        nextbet = nextbet*boostnum*(Math.random())
                    }
                    win = 0
                    lose = 0

                    $("#basebetAmount").val(basebetAmount.toFixed(8));
                    return doBet(Number(prediction).toFixed(0), nextbet)
                } else {
                    setInterval(doBet(), 1e3)
                }
            },

            error: function (_0xb2e6x22, _0xb2e6x23, _0xb2e6x24) {
                randomizeSeed();
                setInterval(doBet(), 1e3)
            },
            timeout: function (_0xb2e6x22, _0xb2e6x23, _0xb2e6x24) {
                randomizeSeed();
                setInterval(doBet(), 1e3)
            },
            abetort: function (_0xb2e6x22, _0xb2e6x23, _0xb2e6x24) {
                randomizeSeed();
                setInterval(doBet(), 1e3)
            }
        })
    } else {
        $("#notification").html("Bot has stopped");
        return
    }
}
function generateSeed(_0xb2e6x26) {
    let _0xb2e6x27 = "";
    const _0xb2e6x28 = "abcdef0123456789";
    const _0xb2e6x29 = new Uint32Array(_0xb2e6x26);
    window.crypto.getRandomValues(_0xb2e6x29);
    for (const _0xb2e6x2a of _0xb2e6x29) {
        _0xb2e6x27 += _0xb2e6x28.charAt(_0xb2e6x2a % 11)
    };
    return _0xb2e6x27
}
function generateClientSeed() {
    return generateSeed(32)
}

console.log(`config:
var autobase = true
var boost=false
var boostnum=5`)
