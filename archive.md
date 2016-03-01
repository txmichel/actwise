---
layout: page
title: Archive
permalink: /archive/
---
What happened so far...

<div class="post-list">
    <ul>
        {% for post in site.posts %}
            <li>
                <a href="{{ post.url }}">
                    {{ post.title }}
                </a>
                <time>{{ post.date | date: '%B %d, %Y' }}</time>
            </li>
        {% endfor %}
    </ul>
</div> <!-- .post-list -->
