# docker-xhgui
Dockerized xhgui, configurable with ENV vars.

## Usage
Run the `tsari/xhgui` container and use the environment vars for configuration.

#### Examples

```
# Link to a docker mongo instance with name "mongo"
docker run --name xhgui --rm -it -p "8000:80" --link mongo tsari/xhgui
```

```
# Use a non-docker mongo db
docker run --name xhgui--rm -it -p "8000:80" -e "XHGUI_MONGO_URI=some-mongo-host:27017" tsari/xhgui
```



| env | description | example | default |
| --- | ----------- | ------- | ------- |
| `XHGUI_MONGO_URI` | the host and port to the mongo db | `XHGUI_MONGO_URI=mongo:27017` | mongo:27017 |
| `XHGUI_MONGO_DB` | the database name for the profiling data | `XHGUI_MONGO_DB=xhprof` | xhprof |

## License

MIT License

Copyright (c) 2017 Tibor Sári

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.