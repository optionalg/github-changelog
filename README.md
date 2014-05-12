github-changelog
====
A simple CSS widget for showing notifications.

## Interface elements ##
### Notification icon ###
This is what shows up by default, before the user has had a chance to interact with the widget.

**Behaviour**
- when no unread notifications are present its styling should reflect this, possibly grayed out or with some default coloring.
- when new notifications are received the icon styling changes to a different, brighter color. Possibly with a glow effect. In addition, a counter will show up displaying the number of new notifications.

### Notification list ###
This list shows the notification area, it will contain number of notification items.

**Behaviour**
- hidden by default, it can be shown or hidden by pressing the *notification icon*.
- if it's visible, it will become hidden if the user interacts with any other part of the page
- it should be able to show up in one of 4 predefined spots in relation to the *notification icon*([see below](#notification-list-1)) according to its CSS class.

### Notification item ###
One element of the notification list.

**Behaviour**
- composed of two elements, a label and text content.
- the label can have different coloring according to its type. Supported types: *'feature'*, *'enhancement'*, *'bug'* 


## HTML Elements ##
### Changelog Wrapper ###
The widget is contained within an element with the class `.changelog-wrapper`
```html
<div class="changelog-wrapper">
...
</div>
```

### Notification icon ###
```html
<a class="btn" href="#">
  Link
  <span class="badge top right">2</span>
</a>
```
Config options via class attribute
- Appearance: as a button `.btn` or a link `.btn-link`. Link appearance won't have border and background color.
- Size: `.small`, `.medium` or `.large`

### Notification counter ###
Contained within the notification icon
```html
<span class="badge round">2</span>
```
Config options via class attribute
- Shape: `.round`(default) or `.square`

### Notification list ###
```html
<!-- List position: (top | bottom | left | right) -->
<div class="top changelog-list-wrapper">
	<ul class="changelog-list">
	...
	</ul>
</div>
```
### Notification item ###
Contained within the notification list
```html
<li>
  <p>
    <!-- #LABEL -->
    <!-- Label type: round (default) | square -->
    <span class="label">featured</span>
    <p>Lorem ipsum dolor sit amet, consectetur.</p>
  </p>
</li>
```
Config options via class attribute
- Shape: `.round`(default) or `square`
- Color: via it's type, can be `feature`, `enhancement`, `bug`, etc.


