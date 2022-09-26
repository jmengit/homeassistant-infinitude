# homeassistant-infinitude
Home Assistant custom component for controlling Carrier Infinity Touch thermostats through an [Infinitude](https://github.com/nebulous/infinitude) proxy server.

# Installation Instructions

## Install Manually

1. Create a `custom_components` directory within your Home Assistant `config` directory if it does not already exist.

2. [Download this repository](https://github.com/jmengit/homeassistant-infinitude2/archive/master.zip).

3. Copy `custom_components/infinitude` from the repository into Home Assistant's `custom_components` directory.

4. Follow the configuration instructions.

## Install with HACS
This custom component can be integrated into [HACS](https://github.com/hacs/integration), so you can track future updates.  If you have do not have have HACS installed, please see [their installation guide](https://hacs.xyz/docs/installation/manual).

1. Select HACS from the left-hand navigation menu.

2. Click _Integrations_.

3. Click the three dots in the upper right-hand corner and select _Custom Repositories_.

4. Paste "https://github.com/jmengit/homeassistant-infinitude2" into the _Add custom repository URL_ text field.

5. Select "Integration" from the Category dropdown and click Add.

6. Close the Custom repositories dialog after it updates with the new integration.

7. "Infinitude2" will appear in your list of repositories.  Click the "Install" link inside it.

8. Click "Install" in the resulting dialog box.

9. Follow the configuration instructions.

# Configuration
Add the following to your `configuration.yaml`:
```yaml
climate:
  - platform: infinitude2
    host: <infinitude_hostname_or_ip>
    port: <optional, defaults to 3000>
    zone_names:
      - Custom Zone Name 1
      - 
      - Custom Zone Name 3
      - ...
```
Custom zone names are optional, and are applied in ascending order (zones 1-8).  If a blank name is provided (like in the second entry above), the zone name is retrieved from the thermostat itself.
