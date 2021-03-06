---
title: Input Methods
layout: en
permalink: docs/references/scripting-api/input/
---

<ul>
	<li>
		<h4 id="clickLocator">click( targetLocator , [ timeout ] , [ recordedImage ] )</h4>
		<p>click on the given locator when it appears on the screen, fails if the locator doesn't appear after given timeout</p>
		<p><ul>
			<li>
				<strong>targetLocator</strong>
				<div>Type: Locator</div>
				<em>the locator to click on</em>
			</li>
			<li>
				<strong>timeout</strong>
				<div>Type: Numeric</div>
				<em>time in seconds to wait until the targetLocator appears, if no set timeout is by default 60 seconds</em>
			</li>
			<li>
				<strong>recordedImage</strong>
				<div>Type: Image</div>
				<em>reference to the screenshots taken during recording</em>
			</li>
		</ul></p>
		<p>
		<strong>Example:</strong>
		{% highlight js %}click(image(4).before().box(129, 469, 221, 69), 60.0, image(4)){% endhighlight %}
		</p>
	</li>
	<li>
		<h4 id="clickPosition">click( x , y , [ recordedImage ] )</h4>
		<p>click immediately on the given position</p>
		<p><ul>
			<li>
				<strong>x</strong>
				<div>Type: Numeric</div>
				<em>x coordinate to click on</em>
			</li>
			<li>
				<strong>y</strong>
				<div>Type: Numeric</div>
				<em>y coordinate to click on</em>
			</li>
			<li>
				<strong>recordedImage</strong>
				<div>Type: Image</div>
				<em>reference to the screenshots taken during recording</em>
			</li>
		</ul></p>
		<p>
		<strong>Example:</strong>
		{% highlight js %}click(100, 100, image(4)){% endhighlight %}
		</p>
	</li>
	<li>
		<h4 id="longPressLocator">longPress( targetLocator , [ timeout ] , [ recordedImage ] )</h4>
		<p>long press on the given locator when it appears on the screen, fails if the locator doesn't appear after given timeout</p>
		<p><ul>
			<li>
				<strong>targetLocator</strong>
				<div>Type: Locator</div>
				<em>the locator to long press on</em>
			</li>
			<li>
				<strong>timeout</strong>
				<div>Type: Numeric</div>
				<em>wait time for the targetLocator to appear in seconds, if no set timeout is by default 60 seconds</em>
			</li>
			<li>
				<strong>recordedImage</strong>
				<div>Type: Image</div>
				<em>reference to the screenshots taken during recording</em>
			</li>
		</ul></p>
		<p>
		<strong>Example:</strong>
		{% highlight js %}longPress(image(4).before().box(129, 469, 221, 69), 60.0, image(4)){% endhighlight %}
		</p>
	</li>
	<li>
		<h4 id"longPressPosition">longPress( x , y , [ recordedImage ] )</h4>
		<p>click immediately on the given position</p>
		<p><ul>
			<li>
				<strong>x</strong>
				<div>Type: Numeric</div>
				<em>x coordinate to long press on</em>
			</li>
			<li>
				<strong>y</strong>
				<div>Type: Numeric</div>
				<em>y coordinate to long press on</em>
			</li>
			<li>
				<strong>recordedImage</strong>
				<div>Type: Image</div>
				<em>reference to the screenshots taken during recording</em>
			</li>
		</ul></p>
		<p>
		<strong>Example:</strong>
		{% highlight js %}longPress(100, 100, image(4)){% endhighlight %}
		</p>
	</li>
	<li>
		<h4 id="drag">drag( flow , [ recordedImage ] )</h4>
		<p>drag using the defined flow, flow is an array containing flow points</p>
		<p><ul>
			<li>
				<strong>flow</strong>
				<div>Type: Array</div>
				<em>2 dimensional array, flow point are triples with x, y coordinates and waitTime in milliseconds</em>
			</li>
			<li>
				<strong>recordedImage</strong>
				<div>Type: Image</div>
				<em>reference to the screenshots taken during recording</em>
			</li>
		</ul></p>
		<p>
		<strong>Example:</strong>
		{% highlight js %}drag([[387, 615, 0], [450, 182, 20]], image(11)){% endhighlight %}
		</p>
	</li>
	<li>
		<h4 id="type">type( text , [ recordedImage ] )</h4>
		<p>type the given text</p>
		<p><ul>
			<li>
				<strong>flow</strong>
				<div>Type: String</div>
				<em>text to be written</em>
			</li>
			<li>
				<strong>recordedImage</strong>
				<div>Type: Image</div>
				<em>reference to the screenshots taken during recording</em>
			</li>
		</ul></p>
		<p>
		<strong>Example:</strong>
		{% highlight js %}type('sample text', image(12)){% endhighlight %}
		</p>
	</li>
	<li>
		<h4 id="randomInput">randomInput( config , [ recordedImage ] )</h4>
		<p>Sends random touch and key events to your application. Fails if an exception (e.g. NullPointerException) is thrown by your application.</p>
		<p><ul>
			<li>
				<strong>config</strong>
				<div>Type: JSON</div>
				<em>json parameters
				    <ul>
					<li>eventCount - number of events to send to your app</li>
					<li>throttle - delay between two events</li>
					<li>seed - Seed value for pseudo-random number generator. If you re-run the randomInput with the same seed value, it will generate the same sequence of events.</li>
				   </ul> 	
				</em>
			</li>
			<li>
				<strong>recordedImage</strong>
				<div>Type: Image</div>
				<em>reference to the screenshots taken during recording</em>
			</li>
		</ul></p>
		<p>
		<strong>Example 1: execute always the same sequence of events</strong>
		{% highlight js %}randomInput({eventCount: 10000, throttle: 0, seed: 123}){% endhighlight %}
		</p>
		<p>
		<strong>Example 2: execute always a different sequence of events</strong>
		{% highlight js %}randomInput({eventCount: 10000, throttle: 0, seed: Math.random() * 100}){% endhighlight %}
		</p>
	</li>
</ul>
