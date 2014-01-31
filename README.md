# Nano-Headers

[Pico](http://pico.dev7studios.com/index.html) Plugin for handling security headers.

### Installation

Start by moving the <code>plugins/nano__headers.php</code> file into your existing Pico install. Then simply configure the headers you would like to apply. The filename contains a double underscore on purpose to ensure it runs before other 'nano_' plugins in the Pico queue. 

The plugin will set as many headers as possible in an attempt to decrease potential security issues. Some headers have specific configuration requirements, like a proper SSL certificate or exhaustive third-party whitelists, and must be enabled manually. Any of the default headers can be disabled by setting the value to <code>false</code>. Learn more about why these headers matter at [securityheaders.com](https://securityheaders.com/).

### Configuration

	$config["nano_headers"] = array(
		"X-Frame-Options" => "SAMEORIGIN",
		"X-XSS-Protection" => "1; mode=block",
		"X-Permitted-Cross-Domain-Policies" => "master-only",
		"X-Content-Type-Options" => "nosniff",
		"Content-Type" => "text/html; charset=utf-8",
		"Content-Security-Policy" => false,
		"Strict-Transport-Security" => false
	);
	
Note: Defining a <code>Content-Security-Policy</code> will also set the synonymous <code>X-WebKit-CSP</code> and <code>X-Content-Security-Policy</code> headers.