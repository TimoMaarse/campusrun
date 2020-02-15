---
layout: index
title: Home
permalink: /
main_nav: true
order: 1
---

<div class="countdown">
    <div class="timer"><b class="countdownvalue" id="countdownA"></b><span class="word" id="countdownTextA"></span></div>
    <div class="timer"><b class="countdownvalue" id="countdownB"></b><span class="word" id="countdownTextB"></span></div>
    <div class="timer"><b class="countdownvalue" id="countdownC"></b><span class="word" id="countdownTextC"></span></div>
    <div class="timer"><b class="countdownvalue" id="countdownD"></b><span class="word" id="countdownTextD"></span></div>
</div>

<script src="/js/countdown.js"></script>
<script src="/js/jquery-3.3.1.min.js"></script>
<script>
    $(document).ready(function() {
        var target_date = new Date(2020, 03, 15, 19, 0, 0);
        var count = new Countdown(target_date, new Date());

        count.countdown(function(time) {
            if (time.days == 0) {
                $("#countdownTextA").html("hours");
                $("#countdownTextB").html("minutes");
                $("#countdownTextC").html("seconds");
                $("#countdownTextD").html("cs");

                $("#countdownA").html(time.hours.toString().padStart(2, "0"));
                $("#countdownB").html(time.minutes.toString().padStart(2, "0"));
                $("#countdownC").html(time.seconds.toString().padStart(2, "0"));
                $("#countdownD").html(time.centiseconds.toString().padStart(2, "0"));
            } else {
                $("#countdownTextA").html("days");
                $("#countdownTextB").html("hours");
                $("#countdownTextC").html("minutes");
                $("#countdownTextD").html("seconds");

                $("#countdownA").html(time.days.toString().padStart(2, "0"));
                $("#countdownB").html(time.hours.toString().padStart(2, "0"));
                $("#countdownC").html(time.minutes.toString().padStart(2, "0"));
                $("#countdownD").html(time.seconds.toString().padStart(2, "0"));
            }
        });
    });
</script>
<style>
    .countdown {
        display: flex;
        justify-content: space-around;
        margin-bottom: 12px;
    }
    @media (max-width: 380px) {
        .countdown {
            display: none;
        }
    }
    .timer {
        padding: 10px;
        text-align: center;
    }
    .countdownvalue {
        display: block;
        font-size: 4rem;
        line-height: 1;
    }
    .word {
        display: block;
    }
</style>

# Campusrun Nijmegen

T.b.a.
