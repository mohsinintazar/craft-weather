# Craft Weather Plugin

The Craft Weather Plugin is a versatile plugin for Craft CMS v3.x that allows you to easily integrate weather information into your Craft-powered websites. This plugin connects to an open-source weather API using an API key to fetch current weather reports for a specific location.

## Features

- **Weather Information**: Retrieve accurate and up-to-date weather information for a specified location.

- **Customizable Templates**: Craft Weather provides customizable templates to display the weather data as you prefer.

## Installation

To install the Craft Weather Plugin, follow these steps:

1. Open your terminal and navigate to your Craft project:
   ```
   cd /path/to/project
   ```

2. Run the following command to download the plugin:
   ```
   composer require mohsin-plugin/craft-weather
   ```

3. In the Craft Control Panel, go to Settings → Plugins and click the "Install" button for the Craft Weather Plugin.

## Configuration

After installation, you need to configure the plugin by providing your API key and location for the weather service in your .env file:

In your project's root directory, create or edit your .env file.

Add the following lines to your .env file, replacing 'your_api_key' with your actual API key and 'your_city' with the location of the city you want to fetch:
```
# Craft Weather Plugin Settings
CRAFT_WEATHER_KEY="your_api_key"
CRAFT_WEATHER_LOCATION="your_city"
```
This configuration allows you to securely store your API key and location outside of the Craft Weather Plugin settings.

## Usage

The Craft Weather Plugin makes it easy to retrieve weather data for a specific location. Here's a basic example of how to use it:

```twig
{% set location = 'Your_Location_Name' %}
{% set weather = craft.weather.getWeather(location) %}

<h2>Weather for {{ location }}</h2>
<p>Temperature: {{ weather.temperature }}°C</p>
<p>Condition: {{ weather.condition }}</p>
<!-- Additional weather data fields can be added here -->
```

You can customize the templates to display the weather data as you see fit.

## Support and Issues

If you encounter any issues or have questions, please visit the [GitHub repository](https://github.com/mohsinintazar/craft-weather) for this plugin. You can also submit bug reports or feature requests there.

## License

The Craft Weather Plugin is open-source and licensed under the [MIT License](LICENSE.md). You are free to use, modify, and distribute it as needed.
