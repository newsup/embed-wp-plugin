<?php
/*
Plugin Name: NewsUp Quiz Embed
Description: Enables shortcode to embed NewsUp quizzes. Usage: <code>[newsup quiz="123"]</code>.
Version: 1.0.1
License: GPLv3
Author: NewsUp
Author URI: http://newsup.com
*/

function createNewsUpEmbedJS($atts, $content = null) {
	extract(shortcode_atts(array(
		'quiz' => ''
	), $atts));

	if (!$quiz) {
		$error = "
		<div style='border: 20px solid red; border-radius: 40px; padding: 40px; margin: 50px 0 70px;'>
			<h3>Error!</h3>
			<p style='margin: 0;'>Something is wrong with your NewsUp shortcode.</p>
		</div>";

		return $error;
	} else {
		$newsupEmbed = "<script async src='//embed.newsup.com/newsupEmbed.js' data-quiz-id='$quiz'></script>";

		return "$newsupEmbed";
	}
}

add_shortcode('newsup', 'createNewsUpEmbedJS');

?>
