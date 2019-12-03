# Write Meow!
It's like twitter, for cats

![right-meow](https://user-images.githubusercontent.com/29616227/70022113-fc2be400-1560-11ea-9582-32fa828b9967.jpg)

## Stack 
- Python 
- HTML 
- CSS
- JS
- Django


## ERD

![twitter-django](https://user-images.githubusercontent.com/29616227/69994719-7be38f80-151c-11ea-90b5-2d76461c3ef1.jpg)

### Sneak peak

```
<div class="media">
	<h3 class="mr-5"><a href="{% url 'posts:for_user' username=post.user.username %}">@{{ post.user.username }}</a></h3>

	<div class="media-body">
		<strong>{{ post.user.username }}</strong>
		<h5>{{ post.message_html|safe }}</h5>
			<time class="time"><a href="{% url 'posts:single' username=post.user.username pk=post.pk %}">{{ post.created_at }}</a></time>
			{% if post.group %}
			<span class="group-name">in <a href="#">{{ post.group.name }}</a></span>
			{% endif %}
		</h5>

		<div class="media-footer">
			{% if user.is_authenticated and post.user == user and not hide_delete %}
				<a href="{% url 'posts:delete' pk=post.pk %}" title="delete" class="btn btn-simple">
					<span class="fa fa-remove text-danger" aria-hidden="true"></span>
					<span class="text-danger icon-label">Delete</span>
				</a>
			{% endif %}
		</div>
	</div>
</div>

```
