# Aspen Discovery Solr Configurations

[![Build Status](https://github.com/bywatersolutions/aspen-solr-configs/workflows/Build%20and%20Test/badge.svg)](https://github.com/bywatersolutions/aspen-solr-configs/actions)
[![Latest Release](https://img.shields.io/github/v/release/bywatersolutions/aspen-solr-configs)](https://github.com/bywatersolutions/aspen-solr-configs/releases/latest)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

Optimized Solr configurations for Aspen Discovery with performance enhancements and multi-version support.

## Features

- **Performance Optimized**: docValues enabled on critical fields for improved faceted search performance
- **Multi-Version Support**: Compatible with Solr 8.11+ and 9.0+
- **Enhanced Suggesters**: BlendedInfixLookupFactory with context-aware filtering
- **Production Ready**: Comprehensive testing and validation

## Supported Versions

| Solr Version | Status |
|--------------|--------|
| 8.11+ | ✅ Supported |
| 9.0+ | ✅ Supported |

## Installation

1. Download the appropriate package for your Solr version from the [releases page](https://github.com/bywatersolutions/aspen-solr-configs/releases)

2. Extract the package:
```bash
tar -xzf aspen-solr-configs-v0.0.1-solr8x.tar.gz
# or
tar -xzf aspen-solr-configs-v0.0.1-solr9x.tar.gz
```

3. Upload configsets to your Solr cluster:
```bash
solr zk upconfig -n grouped_works_v2 -d /path/to/configsets/grouped_works_v2 -z your-zk-host:2181
```

4. Create collections using the configsets:
```bash
curl "http://your-solr:8983/solr/admin/collections?action=CREATE&name=grouped_works&collection.configName=grouped_works_v2&numShards=1&replicationFactor=1"
```

## Available Configsets

- **grouped_works_v2**: Main bibliographic records
- **series**: Series/collection records
- **genealogy**: Genealogical records
- **lists**: User lists and reading history
- **course_reserves**: Course reserve materials
- **events**: Library events and programs
- **open_archives**: Open archives metadata
- **website_pages**: Website content indexing

## Support

For issues or questions:
- [GitHub Issues](https://github.com/bywatersolutions/aspen-solr-configs/issues)
- [ByWater Solutions](https://bywatersolutions.com)

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.
