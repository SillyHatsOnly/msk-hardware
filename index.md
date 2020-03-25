---
layout: default
---

<!-- .......................................

        HEADER

........................................ -->
<div class="header">
    <div class="header__title">Msk-hardware</div>
    <div class="header__slogan">Грустно о весёлом</div>
    <div class="header__arrow">
        <a href="#title"><i class="fa fa-caret-down"></i></a>
    </div>
</div>    


<!-- .......................................

        MAIN PART

........................................ -->
<div class="main__part">
    <div class="container">
        <div id="title" class="title">
            Наши встречи
        </div>
        {% assign rows = site.meetings.size | divided_by: 3.0 | ceil %}
        {% for i in (1..rows) %}
            <div class="row">
            {% assign offset = forloop.index0 | times: 3 %}
            {% for article in site.meetings limit: 3 offset:offset %}
                <div class="col-4">
                    <div class="block">
                        <div class="block-picture">
                            <img src="{{article.preview}}" alt="{{article.title}}">
                        </div>
                        <div class="block-title">
                            <a href="{{article.url}}">{{article.title}}</a>
                        </div>
                    </div>
                </div>
            {% endfor %}
          </div>
        {% endfor %}
    </div>
</div>


<!-- .......................................

        FOOTER

........................................ -->    
<div class="footer">
    <div class="container">
        <div class="row">
            <div class="col-4">
                <p class="footer__name"> Ты печеньки принёс?</p>
                <p> © Сайт создан в 2020.</p>
            </div>
            
            <div class="col-4">
                <p class="footer__social">Мы в сети:</p>
                <p class="footer__social-icons">
                    
                    <a href="https://t.me/joinchat/JGC6v0hbavfAXhmXMZ-6Jg" target="_blank">
                        <i class="fa fa-telegram"></i>
                    </a>
                    
                    <a href="https://www.youtube.com/channel/UCIny9C6BKbhTCSx_4wVQPSQ" target="_blank">
                        <i class="fa fa-youtube"></i>
                    </a>
                    
                    <a href="https://github.com/SillyHatsOnly/sillyhatsonly.github.io" target="_blank">
                        <i class="fa fa-github"></i>
                    </a>
                    
                </p>
            </div>
            <div class="col-4">
                <div><a href="#" class="button">Связь с Космосом</a></div>
                <p>Жми, не жми - всё это пустое...</p>
            </div>
        </div>
    </div>
</div>
