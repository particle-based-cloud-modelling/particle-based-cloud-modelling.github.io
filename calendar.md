---
layout: page
title: Event Calendar
permalink: /calendar/
---
<script src="https://cdnjs.cloudflare.com/ajax/libs/superagent/3.8.3/superagent.min.js" integrity="sha256-tjzBJ0J0qR7dusCFJqxqUyav026cK00fn+Phyaviv0k=" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/fullcalendar/4.0.0-alpha.2/fullcalendar.min.js" integrity="sha256-SX265qsvJdnDUYPKZkL3pCQVclJSZikwT9c1Q6pPkLE=" crossorigin="anonymous"></script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/fullcalendar/4.0.0-alpha.2/fullcalendar.min.css" integrity="sha256-9JXIIG3fFudD4tyIRgOa6MMpId0LJxuIsgrpG1W5NwM=" crossorigin="anonymous" />

<script>
document.addEventListener('DOMContentLoaded', function() {
  var calendarEl = document.getElementById('calendar');
  var calendar = new FullCalendar.Calendar(calendarEl, {
    events: { url: '/calendar-data' }
  });
  calendar.render();
});
</script>

<!--
{% for event in site.events %}
{{event.title}} {{event.event_date}}<br/>
{% endfor %}
-->
<div id="calendar"></div>
