# Nano-Headers

Pico Plugin for handling HTTP headers.

### Configuration

	$config["nano_headers"] = array(
		"X-Frame-Options" => "SAMEORIGIN",
		"X-XSS-Protection" => "1; mode=block",
		"X-Permitted-Cross-Domain-Policies" => "master-only",
		"X-Content-Type-Options" => "nosniff",
		"Content-Security-Policy" => "...",
		"Strict-Transport-Security" => "max-age=15768000",
		"Content-Type" => "text/html; charset=utf-8"
	);