# tunnel.center

`tunnel.center` can be used as an ephemeral reverse proxy for your local
services. This may be useful, for instance when you need to show your friend
something cool you've built.

`tunnel.center` works without installing any software on your machine,
thanks to the magic of Wireguard.


## Usage

To start a tunnel for your local service on port 8080
> Remember to bind your local service to 0.0.0.0

```
curl https://tunnel.center/8080 > tunnel.conf && wg-quick up ./tunnel.conf
```

To stop your tunnel

```
wg-quick down ./tunnel.conf
```


## Self-hosting

Requirements: `python >= 3.9`, `poetry`, `wireguard`, `caddy`.

Use `poetry` to install the dependencies. There is a systemd service
included in the repository as well.


## License


Copyright (C) 2022

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
