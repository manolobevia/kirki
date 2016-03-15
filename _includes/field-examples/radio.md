
{% highlight php %}
<?php
Kirki::add_field( 'my_config', array(
	'type'        => 'radio',
	'settings'    => 'my_setting',
	'label'       => __( 'Radio Control', 'my_textdomain' ),
	'section'     => 'radio',
	'default'     => 'red',
	'priority'    => 10,
	'choices'     => array(
		'red'   => esc_attr__( 'Red', 'my_textdomain' ),
		'green' => esc_attr__( 'Green', 'my_textdomain' ),
		'blue'  => esc_attr__( 'Blue', 'my_textdomain' ),
	),
) );
?>
{% endhighlight %}

In case you need to add additional, extra-long descriptions to your radio options you can use a format like this:

{% highlight php %}
<?php
Kirki::add_field( 'my_config', array(
	'type'        => 'radio',
	'settings'    => 'my_setting',
	'label'       => __( 'Radio Control', 'my_textdomain' ),
	'section'     => 'radio',
	'default'     => 'red',
	'priority'    => 10,
	'choices'     => array(
		'red'   => array(
			esc_attr__( 'Red', 'my_textdomain' ),
			esc_attr__( 'These are some extra details about Red', 'my_textdomain' ),
		),
		'green' => array(
			esc_attr__( 'Green', 'kirki' ),
			esc_attr__( 'These are some extra details about Green', 'my_textdomain' ),
		),
		'blue'  => array(
			esc_attr__( 'Blue', 'kirki' ),
			esc_attr__( 'These are some extra details about Blue', 'my_textdomain' ),
		),
	),
) );
?>
{% endhighlight %}