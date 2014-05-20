github-changelog
====

A widget that provides you with an easy way to send transparent status updates to your customers by tracking a branch on your GitHub repository. Closed issues show up as notifications inside the widget.

## Interface elements ##

![changelog wireframe](https://dl.dropboxusercontent.com/u/42934143/images/changelog2.png)

### Notification icon ###
This is what shows up by default, before the user has had a chance to interact with the widget.

**Behaviour**
- when no unread notifications are present the icon won't be shown.
- when new notifications are received the icon becomes visible. In addition, a counter will show up displaying the number of new notifications.

### Notification list ###
This list shows the notification area, it will contain number of notification items.

**Behaviour**
- hidden by default, it can be shown or hidden by pressing the *notification icon*.
- if it's visible, it will become hidden if the user interacts with any other part of the page
- it can be positioned according with 4 main positions: `top`, `bottom`, `left` and `right`. Each of these positions can be modified by providing a second class: `pull-left` and `pull-right` for vertical positions and `pull-top` for horizontal positions. The purpose here is to make the list usable in any positioning scenario.

**List Positioning**
![list positioning](https://cloud.githubusercontent.com/assets/3300066/2999278/1407e078-dd14-11e3-941c-3cce9f10377c.png)

### Notification item ###
One element of the notification list.

**Behaviour**
- composed of two elements, a label and text content.
- the label can have different coloring according to the label colors set in Github

### HTML ###
**See the HTML Structure [wiki page](https://github.com/uberVU/github-changelog/wiki/HTML-Structure) to get an idea of how these elements will look in HTML**

## Customization options ##
We use LESS to generate the CSS files for the widget. The styles can be easily changed to match your design by tweaking `less/variables.less` and re-generating the CSS. [Grunt](http://gruntjs.com/) can help with [this](https://github.com/gruntjs/grunt-contrib-less).






