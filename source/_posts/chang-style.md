---
title: 更改网站样式
date: 2018-02-05 00:08:53
categories: 分享
---
{% raw %}
<div class="aplayer" id="aplayer-darling"></div>
<script>
$(function () {
    $.ajax({
        url: 'https://api.i-meto.com/meting/api?server=netease&type=song&id=531051597',
        success: function (list) {
            var ap = new APlayer({
                element: document.getElementById('aplayer-darling'),
                showlrc: 3,
                theme: '#ad7a86',
                mode: 'random',
                music: JSON.parse(list)[0]
            });
            window.aplayers || (window.aplayers = []);
            window.aplayers.push(ap);
        }
    })
})
</script>
{% endraw %}
&nbsp;
**点击<a href="javascript:;" id="darling-trigger">这里</a>切换样式**
{% raw %}
<script>
$('#darling-trigger').click(function () {
    var $body = $('body');
    if ($body.hasClass('theme-ievii')) {
        $body.removeClass('theme-ievii');
    }
    else {
        $body.addClass('theme-ievii');
    }
});
</script>
{% endraw %}

![](https://ievii.com/images/ievii-banner01.jpg)
