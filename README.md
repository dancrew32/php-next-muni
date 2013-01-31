# PHP NextMuni

*NextMuni API wrapper written in PHP*

```php

# Instantiate
$nm = new NextMuni;

# Agencies
$agencies = $nm->agency_list()->agency;

# Routes
$nm->agency = 'sf-muni';
$routes = $nm->route_list()->route;

# Configuration (Tons of data)
$nm->route = '38L';
$config = $nm->route_config()->route;

# Predictions
$nm->stop_id = 5555;
$predictions = $nm->predictions()->predictions;

# Multiple Predictions
$nm->stops = array('38L|5555', 'N|4321');
$multi_predictions = $nm->predictions_multiple()->predictions;

# Schedule
$schedule = $nm->schedule();

# Messages
$nm->routes = array('38L', 'N', 'J');
$messages = $nm->messages();

# Vehicle Locations
$locations = $nm->vehicle_locations()->vehicle;


# Instead of building options with magic setters,
# just pass an array of options into NextMuni()
$easy_predictions = new NextMuni(array(
	'agency'  => 'sf-muni',
	'route'   => '38L'
	'stop_id' => 5555
))->predictions()->predictions;

```
