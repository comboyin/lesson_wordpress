# lesson 2
 - Request

Create new field like the picture below:

![Image of Yaktocat](https://github.com/comboyin/lesson_wordpress/blob/master/lession%202/img_readme/create_new_fields.png)

 - New functions: Sanitization setting


register_setting( 'sunset-settings-group', 'twitter_handler', 'sunset_sanitize_twitter_handler' );
 

 //Sanitization settings
function sunset_sanitize_twitter_handler( $input ){
	$output = sanitize_text_field( $input );
	$output = str_replace('@', '', $output);
	return $output;
}
