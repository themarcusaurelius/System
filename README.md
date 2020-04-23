## Collects and parses logs created by the system logging service of common Unix/Linux based distributions.

When you run this module, it performs a few tasks under the hood:

- Sets the default paths to the log files (but don’t worry, you can override the defaults)
- Makes sure each multiline log event gets sent as a single event
- Uses ingest node to parse and process the log lines, shaping the data into a structure suitable for visualizing in Kibana
- Deploys dashboards for visualizing the log data

### Compatibility

This module was tested with logs from OSes like Ubuntu 12.04, Centos 7, and macOS Sierra.

This module is not available for Windows.


## Installation

### Linux:

<i>If you haven't already installed filebeat...</i>

1) Enter the following script into the console using elevated privileges

```
curl https://olympus-io.github.io/vizion.ai/beat-install-scripts/install-config-filebeat.sh> install-config-filebeat.sh; chmod a+x install-config-filebeat.sh; sudo ./install-config-filebeat.sh _PLACEHOLDER_API_ENDPOINT_
```

2) When prompted, select the proper environment to complete the installation.

**Data should now be shipping to your Vizion Elastic app. Check the ```Discover``` tab in Kibana for the incoming logs**

<i>If you have already installed filebeat...</i>

1) Enable the module.

```
filebeat modules enable system
```

2) Restart Filebeat.

```
service filebeat restart
```

**Data should now be shipping to your Vizion Elastic app. Check the ```Discover``` tab in Kibana for the incoming logs**

<hr>

## Example Dashboard

This module comes with sample dashboards. For example:

![Imgur](https://imgur.com/UyvMAgN.png)

