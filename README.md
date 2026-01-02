# Aspen Discovery Solr Configurations

Manually maintained, optimized Solr configurations for Aspen Discovery.

## Overview

This repository contains Solr configsets based on Aspen Discovery with performance optimizations applied manually as needed.

## Installation

```bash
# Download latest release
curl -L -o aspen-solr-configs.tar.gz https://github.com/bywatersolutions/aspen-solr-configs/releases/latest/download/aspen-solr-configs.tar.gz

# Extract to Solr
tar -xzf aspen-solr-configs.tar.gz -C /opt/solr/server/solr/configsets/

# For SolrCloud
solr zk upconfig -n grouped_works_v2 -d /opt/solr/server/solr/configsets/grouped_works_v2 -z localhost:9983
```

## Versioning

- **v0.0.0** - Initial release based on Aspen Discovery 25.Q4.06
- **v0.0.1** - Performance optimizations applied

See `version.yaml` for upstream version tracking.
