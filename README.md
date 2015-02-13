# carrental-wprewrite
this theme was out dated by wordpress in 2012 and I wish to recreate it so it can function again. The creator of the theme no longer supports the theme it was given away free as-is. There are calls that need to be rewritten to make it work again.

Current issues per theme checker.

test site is at http://test.cars4hire.co.nz/

REQUIRED:License: is missing from your style.css header.
REQUIRED:License URI: is missing from your style.css header.
REQUIRED:.sticky css class is needed in your theme css.
REQUIRED:.gallery-caption css class is needed in your theme css.
REQUIRED:.bypostauthor css class is needed in your theme css.
REQUIRED: This theme doesn't seem to display tags. Modify it to display tags in appropriate locations.
RECOMMENDED: Text domain problems in widgets.php. You have not included a text domain!
Line 215: parent::WP_Widget('arbitrarytext', $name = __( 'Text', 'car-rental' ), array('description' => __( 'Arbitrary text with HTML tags and shortcodes')) );
WARNING: The theme uses the add_shortcode() function. Custom post-content shortcodes are plugin-territory functionality.
WARNING: Found proc_open in the file StreamBuffer.php. PHP system calls are often disabled by server admins and should not be in themes.
Line 274: $this->_stream = proc_open($command, $descriptorSpec, $pipes);
WARNING: Found ini_set in the file session.php. Themes should not change server PHP settings.
Line 8: ini_set('session.use_cookies', 'On');
Line 9: ini_set('session.use_trans_sid', 'Off');
Line 10: ini_set('session.save_path', RC_SESSIONS_DIR);
Line 11: ini_set('session.gc_maxlifetime', 86400*$session_lifetime);
Line 12: ini_set('session.cookie_lifetime', 86400*$session_lifetime);
WARNING: Found base64_encode in the file PlainAuthenticator.php. base64_encode() is not allowed.
Line 56: $message = base64_encode($username . chr(0) . $username . chr(0) . $password);
WARNING: Found base64_encode in the file LoginAuthenticator.php. base64_encode() is not allowed.
Line 57: $agent->executeCommand(sprintf('%s\r\n', base64_encode($username)), array(334));
Line 58: $agent->executeCommand(sprintf('%s\r\n', base64_encode($password)), array(235));
WARNING: Found base64_encode in the file CramMd5Authenticator.php. base64_encode() is not allowed.
Line 58: $message = base64_encode(
WARNING: Found base64_encode in the file Base64Encoder.php. base64_encode() is not allowed.
Line 50: $encodedString = base64_encode($string);
WARNING: Found base64_encode in the file Base64ContentEncoder.php. base64_encode() is not allowed.
Line 57: $encoded = base64_encode($bytes);
WARNING: Found base64_decode in the file CramMd5Authenticator.php. base64_decode() is not allowed.
Line 57: $challenge = base64_decode(substr($challenge, 4));
WARNING: fwrite was found in the file StreamBuffer.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 219: && fwrite($this->_in, $bytes))
WARNING: fwrite was found in the file PopBeforeSmtpPlugin.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 253: if (!fwrite($this->_socket, $command))
WARNING: fwrite was found in the file FileByteStream.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 127: fwrite($this->_getWriteHandle(), $bytes);
WARNING: fwrite was found in the file DiskKeyCache.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 111: fwrite($fp, $string);
Line 144: fwrite($fp, $bytes);
WARNING: fwrite was found in the file ArrayCharacterStream.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 224: fwrite($fp, $chars);
WARNING: fsockopen was found in the file StreamBuffer.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 243: if (!$this->_stream = fsockopen($host, $this->_params['port'], $errno, $errstr, $timeout))
WARNING: fsockopen was found in the file PopBeforeSmtpPlugin.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 160: if (!$socket = fsockopen(
WARNING: fread was found in the file StreamBuffer.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 194: $ret = fread($this->_out, $length);
WARNING: fread was found in the file FileByteStream.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 94: $bytes = fread($fp, $length);
WARNING: fread was found in the file DiskKeyCache.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 187: while (!feof($fp) && false !== $bytes = fread($fp, 8192))
Line 214: while (!feof($fp) && false !== $bytes = fread($fp, 8192))
WARNING: fread was found in the file ArrayCharacterStream.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 323: if (!feof($fp) && ($bytes = fread($fp, $len)) !== false)
WARNING: fopen was found in the file FileByteStream.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 141: if (!$this->_reader = fopen($this->_path, 'rb'))
Line 157: if (!$this->_writer = fopen($this->_path, $this->_mode))
WARNING: fopen was found in the file DiskKeyCache.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 301: $fp = fopen($this->_path . '/' . $nsKey . '/' . $itemKey, 'w+b');
WARNING: fopen was found in the file ArrayCharacterStream.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 223: $fp = fopen('php://memory', 'w+b');
WARNING: fclose was found in the file StreamBuffer.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 123: fclose($this->_in);
Line 124: fclose($this->_out);
Line 129: fclose($this->_stream);
WARNING: fclose was found in the file PopBeforeSmtpPlugin.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 199: if (!fclose($this->_socket))
WARNING: fclose was found in the file FileByteStream.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 172: fclose($this->_writer);
Line 182: fclose($this->_reader);
WARNING: fclose was found in the file DiskKeyCache.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 246: fclose($fp);
WARNING: fclose was found in the file ArrayCharacterStream.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 284: fclose($fp);
WARNING: curl_init was found in the file currency.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 142: $ch = curl_init();
WARNING: curl_exec was found in the file currency.php File operations should use the WP_Filesystem methods instead of direct PHP filesystem calls.
Line 146: $content = curl_exec($ch);
REQUIRED: The <title> tags can only contain a call to wp_title(). Use the wp_title filter to modify the output
REQUIRED: No content width has been defined. Example:
if ( ! isset( $content_width ) ) $content_width = 900;
REQUIRED: Could not find wp_link_pages. See: wp_link_pages
 <?php wp_link_pages( $args ); ?>
REQUIRED: Could not find comment_form. See: comment_form
 <?php comment_form(); ?>
REQUIRED: Could not find body_class call in body tag. See: body_class
 <?php body_class( $class ); ?>
REQUIRED: startup.php. Themes should use add_theme_page() for adding admin pages.
Line 22: if (function_exists('add_menu_page')) {
Line 23: add_menu_page(__( 'Car Rental', 'car-rental' ), __( 'Car Rental', 'car-rent
REQUIRED: register_widget_control() found in the file widgets.php. Deprecated since version 2.8. Use wp_register_widget_control() instead.
Line 39: register_widget_control( __( 'Blog', 'car-rental' ), 'rc_blog_widget_admin'
Line 304: register_widget_control( __( 'FAQ', 'car-rental' ), 'rc_faq_widget_admin');
Line 424: register_widget_control( __( 'Subpages', 'car-rental' ), 'rc_subpages_widge
REQUIRED: register_sidebar_widget() found in the file widgets.php. Deprecated since version 2.8. Use wp_register_sidebar_widget() instead.
Line 8: register_sidebar_widget( __( 'Blog', 'car-rental' ), 'rc_blog_widget' );
Line 284: register_sidebar_widget( __( 'FAQ', 'car-rental' ), 'rc_faq_widget' );
Line 400: register_sidebar_widget( __( 'Subpages', 'car-rental' ), 'rc_subpages_widge
REQUIRED: get_option(home) was found in the file footer.php. Use home_url() instead.
REQUIRED: get_option('home') was found in the file header.php. Use home_url() instead.
Line 154: <a href='<?php echo get_option('home'); ?>'><img src='<?php echo RC_UPLOADS_URL .'logo_'.$logot
Line 156: <a href='<?php echo get_option('home'); ?>'><img src='<?php echo RC_FRONT_IMAGES_URL; ?>logotyp
Line 175: <li><a href='<?php echo get_option('home'); ?>'><?php _e( 'Home', 'car-rental' ); ?></a></li>
REQUIRED: get_option('home') was found in the file footer.php. Use home_url() instead.
Line 27: <?php $copyright = str_replace(array('[url]','[/url]'), array('<a href=''.get_option('home').''>','</a>'), get_option('rc_settings_footer_copyright')
REQUIRED: get_bloginfo('template_url') was found in the file functions.php. Use get_template_directory_uri() instead.
Line 30: define('RC_TEMPLATE_URL',  get_bloginfo('template_url'));
REQUIRED: bloginfo('template_url') was found in the file functions.php. Use echo esc_url( get_template_directory_uri() ) instead.
Line 30: define('RC_TEMPLATE_URL',  get_bloginfo('template_url'));
REQUIRED: get_option(home) was found in the file header.php. Use home_url() instead.
RECOMMENDED: could not find the file readme.txt in the theme. Please see Theme_Documentation for more information.
RECOMMENDED: Screenshot size should be 880x660, to account for HiDPI displays. Any 4:3 image size is acceptable, but 880x660 is preferred.
RECOMMENDED: Screenshot dimensions are wrong! Ratio of width to height should be 4:3.
RECOMMENDED: No reference to add_theme_support( "title-tag" ) was found in the theme. It is recommended that the theme implement this functionality for WordPress 4.1 and above.
RECOMMENDED: No reference to add_theme_support( "custom-header", $args ) was found in the theme. It is recommended that the theme implement this functionality if using an image for the header.
RECOMMENDED: No reference to add_theme_support( "custom-background", $args ) was found in the theme. If the theme uses background images or solid colors for the background, then it is recommended that the theme implement this functionality.
RECOMMENDED: get_bloginfo(template_url) was found in the file functions.php. Use get_template_directory_uri() instead.
RECOMMENDED: Tags: is either empty or missing in style.css header.
RECOMMENDED: TEMPLATEPATH was found in the file functions.php. Use get_template_directory() instead.
Line 8: define('RC_INSTALL_DIR', TEMPLATEPATH . '/install/');
Line 11: define('RC_LIBRARIES_DIR', TEMPLATEPATH . '/system/libraries/');
Line 12: define('RC_HELPERS_DIR', TEMPLATEPATH . '/system/helpers/');
Line 16: define('RC_ADMIN_DIR', TEMPLATEPATH . '/admin/');
Line 17: define('RC_ADMIN_CLASSES_DIR', TEMPLATEPATH . '/admin/classes/');
Line 18: define('RC_ADMIN_FUNCTIONS_DIR', TEMPLATEPATH . '/admin/functions/');
Line 19: define('RC_ADMIN_TEMPLATES_DIR', TEMPLATEPATH . '/admin/templates/');
Line 20: define('RC_ADMIN_CSS_DIR', TEMPLATEPATH . '/admin/templates/css/');
Line 23: define('RC_FRONT_DIR', TEMPLATEPATH . '/front/');
Line 24: define('RC_FRONT_CLASSES_DIR', TEMPLATEPATH . '/front/classes/');
Line 25: define('RC_FRONT_FUNCTIONS_DIR', TEMPLATEPATH . '/front/functions/');
Line 26: define('RC_FRONT_TEMPLATES_DIR', TEMPLATEPATH . '/front/templates/');
Line 27: define('RC_FRONT_CSS_DIR', TEMPLATEPATH . '/front/templates/css/');
Line 304: load_theme_textdomain( 'car-rental', TEMPLATEPATH . '/languages' );
Line 307: $locale_file = TEMPLATEPATH . '/languages/$locale.php';
Line 382: require_once(TEMPLATEPATH . '/widgets.php');
INFO: Non-printable characters were found in the bookings.php file. You may want to check this file for errors.
Line 1113: $data['data']['currency_id']['title'] = __( '??urrency:', 'car-rental' );
INFO: At least one hard coded date was found in the file single.php. Consider get_option( 'date_format' ) instead.
INFO: At least one hard coded date was found in the file category.php. Consider get_option( 'date_format' ) instead.
INFO: template.php The theme appears to use include or require. If these are being used to include separate sections of a template from independent files, then get_template_part() should be used instead.
Line 22: require($file);
INFO: startup.php The theme appears to use include or require. If these are being used to include separate sections of a template from independent files, then get_template_part() should be used instead.
Line 12: require_once(RC_FRONT_CLASSES_DIR . 'customer.php');
Line 20: require_once(RC_FRONT_FUNCTIONS_DIR . 'shortcodes.php');
Line 23: require_once(RC_FRONT_FUNCTIONS_DIR . 'fix.php');
Line 49: require_once(RC_FRONT_FUNCTIONS_DIR . 'homepage.php');
Line 53: require_once(RC_FRONT_FUNCTIONS_DIR . 'get_quote.php');
Line 57: require_once(RC_FRONT_FUNCTIONS_DIR . 'booking.php');
Line 61: require_once(RC_FRONT_FUNCTIONS_DIR . 'contacts.php');
INFO: startup.php The theme appears to use include or require. If these are being used to include separate sections of a template from independent files, then get_template_part() should be used instead.
Line 12: require_once(RC_ADMIN_CLASSES_DIR . 'pagination.php');
Line 69: require_once(RC_ADMIN_FUNCTIONS_DIR . 'metaboxes.php');
Line 85: require_once(RC_ADMIN_FUNCTIONS_DIR . 'bookings.php');
Line 89: require_once(RC_ADMIN_FUNCTIONS_DIR . 'customers.php');
Line 93: require_once(RC_ADMIN_FUNCTIONS_DIR . 'vehicles.php');
Line 97: require_once(RC_ADMIN_FUNCTIONS_DIR . 'adverts.php');
Line 101: require_once(RC_ADMIN_FUNCTIONS_DIR . 'localization.php');
Line 105: require_once(RC_ADMIN_FUNCTIONS_DIR . 'settings.php');
Line 109: require_once(RC_ADMIN_FUNCTIONS_DIR . 'help.php');
INFO: settings.php The theme appears to use include or require. If these are being used to include separate sections of a template from independent files, then get_template_part() should be used instead.
Line 27: require_once(RC_ADMIN_FUNCTIONS_DIR . 'settings-system.php');
Line 32: require_once(RC_ADMIN_FUNCTIONS_DIR . 'settings-layout.php');
Line 37: require_once(RC_ADMIN_FUNCTIONS_DIR . 'settings-homepage.php');
Line 42: require_once(RC_ADMIN_FUNCTIONS_DIR . 'settings-contact.php');
INFO: settings-system.php The theme appears to use include or require. If these are being used to include separate sections of a template from independent files, then get_template_part() should be used instead.
Line 35: require_once(RC_ADMIN_FUNCTIONS_DIR . 'settings-system-general.php');
Line 40: require_once(RC_ADMIN_FUNCTIONS_DIR . 'settings-system-emails.php');
Line 45: require_once(RC_ADMIN_FUNCTIONS_DIR . 'settings-system-countries.php');
Line 50: require_once(RC_ADMIN_FUNCTIONS_DIR . 'settings-system-currencies.php');
Line 55: require_once(RC_ADMIN_FUNCTIONS_DIR . 'settings-system-locations.php');
INFO: ajax.php The theme appears to use include or require. If these are being used to include separate sections of a template from independent files, then get_template_part() should be used instead.
Line 18: require_once($wp_root.'/wp-load.php');
Line 20: require_once($wp_root.'/wp-config.php');
Line 29: require_once(RC_LIBRARIES_DIR . 'registry.php');
Line 32: require_once(RC_LIBRARIES_DIR . 'buffer.php');
Line 36: require_once(RC_LIBRARIES_DIR . 'request.php');
Line 40: require_once(RC_LIBRARIES_DIR . 'session.php');
Line 44: require_once(RC_LIBRARIES_DIR . 'currency.php');
Line 48: require_once(RC_HELPERS_DIR.'swift/swift_required.php'); 
Line 52: require_once(RC_LIBRARIES_DIR . 'json.php');
Line 55: require_once(RC_LIBRARIES_DIR . 'template.php');
Line 58: require_once(RC_LIBRARIES_DIR . 'image.php');
Line 59: require_once(RC_HELPERS_DIR . 'image.php');
Line 80: require_once(RC_FRONT_FUNCTIONS_DIR . 'contacts.php');
Line 84: require_once(RC_FRONT_FUNCTIONS_DIR . 'booking.php');
INFO: ajax.php The theme appears to use include or require. If these are being used to include separate sections of a template from independent files, then get_template_part() should be used instead.
Line 17: require_once($wp_root.'/wp-load.php');
Line 19: require_once($wp_root.'/wp-config.php');
Line 34: require_once(RC_LIBRARIES_DIR . 'registry.php');
Line 37: require_once(RC_LIBRARIES_DIR . 'buffer.php');
Line 41: require_once(RC_LIBRARIES_DIR . 'request.php');
Line 45: require_once(RC_LIBRARIES_DIR . 'currency.php');
Line 49: require_once(RC_LIBRARIES_DIR . 'json.php');
Line 60: require_once(RC_ADMIN_FUNCTIONS_DIR . 'vehicles.php');
Line 64: require_once(RC_ADMIN_FUNCTIONS_DIR . 'bookings.php');
INFO: adverts.php The theme appears to use include or require. If these are being used to include separate sections of a template from independent files, then get_template_part() should be used instead.
Line 27: require_once(RC_ADMIN_FUNCTIONS_DIR . 'adverts-slider.php');
Line 32: require_once(RC_ADMIN_FUNCTIONS_DIR . 'adverts-sidebar.php');
