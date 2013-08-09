---
title: Apps Methods
layout: en
permalink: apps/
---

<ul>
	<li>
		<h4>installApp( appId )</h3>
		<p>install the dependency with the given id</p>
		<p><ul>
			<li>
				<strong>appId</strong>
				<div>Type: Numeric</div>
				<em>id of the dependency</em>
			</li>
		</ul></p>
		<p>
		<strong>Example:</strong>
		{% highlight js %}installApp(1){% endhighlight %}
		</p>
	</li>
	<li>
		<h4>launchDefaultApp()</h3>
		<p>launch the default app of the current project</p>
		<strong>Example:</strong>
		{% highlight js %}launchDefaultApp(){% endhighlight %}
		</p>
	</li>
	<li>
		<h4>restartDefaultApp()</h3>
		<p>restart the default app of the current project</p>
		<strong>Example:</strong>
		{% highlight js %}restartDefaultApp(){% endhighlight %}
		</p>
	</li>
</ul>