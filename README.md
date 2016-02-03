# NodeSource Docker Images

![nodesource](./brand/nodesource.png) ![nodejs](./brand/nodejs.png) ![docker](./brand/docker.png)

The NodeSource docker images deliver [NodeSource's deb and rpm](deb.nodesource.com) packages across all of our supported platforms! We offer version pinning, allowing your project to track major, minor, or patch versions of Node or iojs.

# Usage

Use any one of our images as a base for your image. We suggest caching your `package.json` and `npm install` in layers to reduce build time:

```Dockerfile
FROM nodesource/jessie:0.12.7

# cache package.json and node_modules to speed up builds
ADD package.json package.json
RUN npm install

# Add your source files
ADD . .
CMD ["npm","start"]
```

# Notes

* `NODE_ENV` is set to `production` on these images. If you are using these images for development work, add the line: `ENV NODE_ENV dev` to your `Dockerfile`.

# Images

We offer tags for tracking major and minor releases. These tags enable you to receive either security patches or new features, while avoiding breaking changes.

Note: some images may not have all tags, if a major/minor version is not supported on a particular release, these tags will not work.
For example, Ubuntu Precise does not have any iojs tags, and Ubuntu Vivid does not have any tags before iojs-1.8.1.

* `latest` points to the latest release of Node
* `LTS` points to the latest LTS release of Node
* `argon` points to the named LTS release of Node
* `X` points to the latest release of Node X
* `X.Y` points to the latest release of Node X.Y
* `iojs` points to the latest release of iojs
* `iojs-X` points to the latest minor release of iojs-X
* `iojs-X.Y` points to the latest patch release of iojs-X.Y

## Debian-based images

* [**Debian wheezy**](https://registry.hub.docker.com/u/nodesource/wheezy/) - `docker pull nodesource/wheezy`
  * Node 0.10.30 - `docker pull nodesource/wheezy:0.10.30`
  * Node 0.10.31 - `docker pull nodesource/wheezy:0.10.31`
  * Node 0.10.32 - `docker pull nodesource/wheezy:0.10.32`
  * Node 0.10.33 - `docker pull nodesource/wheezy:0.10.33`
  * Node 0.10.34 - `docker pull nodesource/wheezy:0.10.34`
  * Node 0.10.35 - `docker pull nodesource/wheezy:0.10.35`
  * Node 0.10.36 - `docker pull nodesource/wheezy:0.10.36`
  * Node 0.10.37 - `docker pull nodesource/wheezy:0.10.37`
  * Node 0.10.38 - `docker pull nodesource/wheezy:0.10.38`
  * Node 0.10.39 - `docker pull nodesource/wheezy:0.10.39`
  * Node 0.10.40 - `docker pull nodesource/wheezy:0.10.40`
  * Node 0.10.41 - `docker pull nodesource/wheezy:0.10.41`
  * Node 0.12.0 - `docker pull nodesource/wheezy:0.12.0`
  * Node 0.12.2 - `docker pull nodesource/wheezy:0.12.2`
  * Node 0.12.3 - `docker pull nodesource/wheezy:0.12.3`
  * Node 0.12.4 - `docker pull nodesource/wheezy:0.12.4`
  * Node 0.12.5 - `docker pull nodesource/wheezy:0.12.5`
  * Node 0.12.6 - `docker pull nodesource/wheezy:0.12.6`
  * Node 0.12.7 - `docker pull nodesource/wheezy:0.12.7`
  * Node 0.12.8 - `docker pull nodesource/wheezy:0.12.8`
  * Node 0.12.9 - `docker pull nodesource/wheezy:0.12.9`
  * Node 4.1.1 - `docker pull nodesource/wheezy:4.1.1`
  * Node 4.1.2 - `docker pull nodesource/wheezy:4.1.2`
  * Node 4.2.0 - `docker pull nodesource/wheezy:4.2.0`
  * Node 4.2.1 - `docker pull nodesource/wheezy:4.2.1`
  * Node 4.2.2 - `docker pull nodesource/wheezy:4.2.2`
  * Node 4.2.3 - `docker pull nodesource/wheezy:4.2.3`
  * Node 4.2.4 - `docker pull nodesource/wheezy:4.2.4`
  * Node 4.2.5 - `docker pull nodesource/wheezy:4.2.5`
  * Node 4.2.6 - `docker pull nodesource/wheezy:4.2.6`
  * Node 5.0.0 - `docker pull nodesource/wheezy:5.0.0`
  * Node 5.1.0 - `docker pull nodesource/wheezy:5.1.0`
  * Node 5.1.1 - `docker pull nodesource/wheezy:5.1.1`
  * Node 5.2.0 - `docker pull nodesource/wheezy:5.2.0`
  * Node 5.3.0 - `docker pull nodesource/wheezy:5.3.0`
  * Node 5.4.0 - `docker pull nodesource/wheezy:5.4.0`
  * Node 5.4.1 - `docker pull nodesource/wheezy:5.4.1`
  * Node 5.5.0 - `docker pull nodesource/wheezy:5.5.0`
* [**Debian jessie**](https://registry.hub.docker.com/u/nodesource/jessie/) - `docker pull nodesource/jessie`
  * Node 0.10.30 - `docker pull nodesource/jessie:0.10.30`
  * Node 0.10.31 - `docker pull nodesource/jessie:0.10.31`
  * Node 0.10.32 - `docker pull nodesource/jessie:0.10.32`
  * Node 0.10.33 - `docker pull nodesource/jessie:0.10.33`
  * Node 0.10.34 - `docker pull nodesource/jessie:0.10.34`
  * Node 0.10.35 - `docker pull nodesource/jessie:0.10.35`
  * Node 0.10.36 - `docker pull nodesource/jessie:0.10.36`
  * Node 0.10.37 - `docker pull nodesource/jessie:0.10.37`
  * Node 0.10.38 - `docker pull nodesource/jessie:0.10.38`
  * Node 0.10.39 - `docker pull nodesource/jessie:0.10.39`
  * Node 0.10.40 - `docker pull nodesource/jessie:0.10.40`
  * Node 0.10.41 - `docker pull nodesource/jessie:0.10.41`
  * Node 0.12.0 - `docker pull nodesource/jessie:0.12.0`
  * Node 0.12.2 - `docker pull nodesource/jessie:0.12.2`
  * Node 0.12.3 - `docker pull nodesource/jessie:0.12.3`
  * Node 0.12.4 - `docker pull nodesource/jessie:0.12.4`
  * Node 0.12.5 - `docker pull nodesource/jessie:0.12.5`
  * Node 0.12.6 - `docker pull nodesource/jessie:0.12.6`
  * Node 0.12.7 - `docker pull nodesource/jessie:0.12.7`
  * Node 0.12.8 - `docker pull nodesource/jessie:0.12.8`
  * Node 0.12.9 - `docker pull nodesource/jessie:0.12.9`
  * Node 4.0.0 - `docker pull nodesource/jessie:4.0.0`
  * Node 4.1.0 - `docker pull nodesource/jessie:4.1.0`
  * Node 4.1.1 - `docker pull nodesource/jessie:4.1.1`
  * Node 4.1.2 - `docker pull nodesource/jessie:4.1.2`
  * Node 4.2.0 - `docker pull nodesource/jessie:4.2.0`
  * Node 4.2.1 - `docker pull nodesource/jessie:4.2.1`
  * Node 4.2.2 - `docker pull nodesource/jessie:4.2.2`
  * Node 4.2.3 - `docker pull nodesource/jessie:4.2.3`
  * Node 4.2.4 - `docker pull nodesource/jessie:4.2.4`
  * Node 4.2.5 - `docker pull nodesource/jessie:4.2.5`
  * Node 4.2.6 - `docker pull nodesource/jessie:4.2.6`
  * Node 5.0.0 - `docker pull nodesource/jessie:5.0.0`
  * Node 5.1.0 - `docker pull nodesource/jessie:5.1.0`
  * Node 5.1.1 - `docker pull nodesource/jessie:5.1.1`
  * Node 5.2.0 - `docker pull nodesource/jessie:5.2.0`
  * Node 5.3.0 - `docker pull nodesource/jessie:5.3.0`
  * Node 5.4.0 - `docker pull nodesource/jessie:5.4.0`
  * Node 5.4.1 - `docker pull nodesource/jessie:5.4.1`
  * Node 5.5.0 - `docker pull nodesource/jessie:5.5.0`
  * iojs 1.3.0 - `docker pull nodesource/jessie:iojs-1.3.0`
  * iojs 1.4.1 - `docker pull nodesource/jessie:iojs-1.4.1`
  * iojs 1.4.2 - `docker pull nodesource/jessie:iojs-1.4.2`
  * iojs 1.4.3 - `docker pull nodesource/jessie:iojs-1.4.3`
  * iojs 1.5.0 - `docker pull nodesource/jessie:iojs-1.5.0`
  * iojs 1.5.1 - `docker pull nodesource/jessie:iojs-1.5.1`
  * iojs 1.6.1 - `docker pull nodesource/jessie:iojs-1.6.1`
  * iojs 1.6.2 - `docker pull nodesource/jessie:iojs-1.6.2`
  * iojs 1.6.3 - `docker pull nodesource/jessie:iojs-1.6.3`
  * iojs 1.6.4 - `docker pull nodesource/jessie:iojs-1.6.4`
  * iojs 1.7.1 - `docker pull nodesource/jessie:iojs-1.7.1`
  * iojs 1.8.1 - `docker pull nodesource/jessie:iojs-1.8.1`
  * iojs 1.8.3 - `docker pull nodesource/jessie:iojs-1.8.3`
  * iojs 1.8.4 - `docker pull nodesource/jessie:iojs-1.8.4`
  * iojs 2.0.0 - `docker pull nodesource/jessie:iojs-2.0.0`
  * iojs 2.0.1 - `docker pull nodesource/jessie:iojs-2.0.1`
  * iojs 2.0.2 - `docker pull nodesource/jessie:iojs-2.0.2`
  * iojs 2.1.0 - `docker pull nodesource/jessie:iojs-2.1.0`
  * iojs 2.2.1 - `docker pull nodesource/jessie:iojs-2.2.1`
  * iojs 2.3.0 - `docker pull nodesource/jessie:iojs-2.3.0`
  * iojs 2.3.1 - `docker pull nodesource/jessie:iojs-2.3.1`
  * iojs 2.3.2 - `docker pull nodesource/jessie:iojs-2.3.2`
  * iojs 2.3.3 - `docker pull nodesource/jessie:iojs-2.3.3`
  * iojs 2.3.4 - `docker pull nodesource/jessie:iojs-2.3.4`
  * iojs 2.4.0 - `docker pull nodesource/jessie:iojs-2.4.0`
  * iojs 2.5.0 - `docker pull nodesource/jessie:iojs-2.5.0`
  * iojs 3.0.0 - `docker pull nodesource/jessie:iojs-3.0.0`
  * iojs 3.1.0 - `docker pull nodesource/jessie:iojs-3.1.0`
  * iojs 3.2.0 - `docker pull nodesource/jessie:iojs-3.2.0`
  * iojs 3.3.0 - `docker pull nodesource/jessie:iojs-3.3.0`
* [**Debian sid**](https://registry.hub.docker.com/u/nodesource/sid/) - `docker pull nodesource/sid`
  * Node 0.10.30 - `docker pull nodesource/sid:0.10.30`
  * Node 0.10.31 - `docker pull nodesource/sid:0.10.31`
  * Node 0.10.32 - `docker pull nodesource/sid:0.10.32`
  * Node 0.10.33 - `docker pull nodesource/sid:0.10.33`
  * Node 0.10.34 - `docker pull nodesource/sid:0.10.34`
  * Node 0.10.35 - `docker pull nodesource/sid:0.10.35`
  * Node 0.10.36 - `docker pull nodesource/sid:0.10.36`
  * Node 0.10.37 - `docker pull nodesource/sid:0.10.37`
  * Node 0.10.38 - `docker pull nodesource/sid:0.10.38`
  * Node 0.10.39 - `docker pull nodesource/sid:0.10.39`
  * Node 0.10.40 - `docker pull nodesource/sid:0.10.40`
  * Node 0.10.41 - `docker pull nodesource/sid:0.10.41`
  * Node 0.12.0 - `docker pull nodesource/sid:0.12.0`
  * Node 0.12.2 - `docker pull nodesource/sid:0.12.2`
  * Node 0.12.3 - `docker pull nodesource/sid:0.12.3`
  * Node 0.12.4 - `docker pull nodesource/sid:0.12.4`
  * Node 0.12.5 - `docker pull nodesource/sid:0.12.5`
  * Node 0.12.6 - `docker pull nodesource/sid:0.12.6`
  * Node 0.12.7 - `docker pull nodesource/sid:0.12.7`
  * Node 0.12.8 - `docker pull nodesource/sid:0.12.8`
  * Node 0.12.9 - `docker pull nodesource/sid:0.12.9`
  * Node 4.0.0 - `docker pull nodesource/sid:4.0.0`
  * Node 4.1.0 - `docker pull nodesource/sid:4.1.0`
  * Node 4.1.1 - `docker pull nodesource/sid:4.1.1`
  * Node 4.1.2 - `docker pull nodesource/sid:4.1.2`
  * Node 4.2.0 - `docker pull nodesource/sid:4.2.0`
  * Node 4.2.1 - `docker pull nodesource/sid:4.2.1`
  * Node 4.2.2 - `docker pull nodesource/sid:4.2.2`
  * Node 4.2.3 - `docker pull nodesource/sid:4.2.3`
  * Node 4.2.4 - `docker pull nodesource/sid:4.2.4`
  * Node 4.2.5 - `docker pull nodesource/sid:4.2.5`
  * Node 4.2.6 - `docker pull nodesource/sid:4.2.6`
  * Node 5.0.0 - `docker pull nodesource/sid:5.0.0`
  * Node 5.1.0 - `docker pull nodesource/sid:5.1.0`
  * Node 5.1.1 - `docker pull nodesource/sid:5.1.1`
  * Node 5.2.0 - `docker pull nodesource/sid:5.2.0`
  * Node 5.3.0 - `docker pull nodesource/sid:5.3.0`
  * Node 5.4.0 - `docker pull nodesource/sid:5.4.0`
  * Node 5.4.1 - `docker pull nodesource/sid:5.4.1`
  * Node 5.5.0 - `docker pull nodesource/sid:5.5.0`
  * iojs 1.3.0 - `docker pull nodesource/sid:iojs-1.3.0`
  * iojs 1.4.1 - `docker pull nodesource/sid:iojs-1.4.1`
  * iojs 1.4.2 - `docker pull nodesource/sid:iojs-1.4.2`
  * iojs 1.4.3 - `docker pull nodesource/sid:iojs-1.4.3`
  * iojs 1.5.0 - `docker pull nodesource/sid:iojs-1.5.0`
  * iojs 1.5.1 - `docker pull nodesource/sid:iojs-1.5.1`
  * iojs 1.6.1 - `docker pull nodesource/sid:iojs-1.6.1`
  * iojs 1.6.2 - `docker pull nodesource/sid:iojs-1.6.2`
  * iojs 1.6.3 - `docker pull nodesource/sid:iojs-1.6.3`
  * iojs 1.6.4 - `docker pull nodesource/sid:iojs-1.6.4`
  * iojs 1.7.1 - `docker pull nodesource/sid:iojs-1.7.1`
  * iojs 1.8.1 - `docker pull nodesource/sid:iojs-1.8.1`
  * iojs 1.8.3 - `docker pull nodesource/sid:iojs-1.8.3`
  * iojs 1.8.4 - `docker pull nodesource/sid:iojs-1.8.4`
  * iojs 2.0.0 - `docker pull nodesource/sid:iojs-2.0.0`
  * iojs 2.0.1 - `docker pull nodesource/sid:iojs-2.0.1`
  * iojs 2.0.2 - `docker pull nodesource/sid:iojs-2.0.2`
  * iojs 2.1.0 - `docker pull nodesource/sid:iojs-2.1.0`
  * iojs 2.2.1 - `docker pull nodesource/sid:iojs-2.2.1`
  * iojs 2.3.0 - `docker pull nodesource/sid:iojs-2.3.0`
  * iojs 2.3.1 - `docker pull nodesource/sid:iojs-2.3.1`
  * iojs 2.3.2 - `docker pull nodesource/sid:iojs-2.3.2`
  * iojs 2.3.3 - `docker pull nodesource/sid:iojs-2.3.3`
  * iojs 2.3.4 - `docker pull nodesource/sid:iojs-2.3.4`
  * iojs 2.4.0 - `docker pull nodesource/sid:iojs-2.4.0`
  * iojs 2.5.0 - `docker pull nodesource/sid:iojs-2.5.0`
  * iojs 3.0.0 - `docker pull nodesource/sid:iojs-3.0.0`
  * iojs 3.1.0 - `docker pull nodesource/sid:iojs-3.1.0`
  * iojs 3.2.0 - `docker pull nodesource/sid:iojs-3.2.0`
  * iojs 3.3.0 - `docker pull nodesource/sid:iojs-3.3.0`

## Ubuntu-based images

* [**Ubuntu precise**](https://registry.hub.docker.com/u/nodesource/precise/) - `docker pull nodesource/precise`
  * Node 0.10.30 - `docker pull nodesource/precise:0.10.30`
  * Node 0.10.31 - `docker pull nodesource/precise:0.10.31`
  * Node 0.10.32 - `docker pull nodesource/precise:0.10.32`
  * Node 0.10.33 - `docker pull nodesource/precise:0.10.33`
  * Node 0.10.34 - `docker pull nodesource/precise:0.10.34`
  * Node 0.10.35 - `docker pull nodesource/precise:0.10.35`
  * Node 0.10.36 - `docker pull nodesource/precise:0.10.36`
  * Node 0.10.37 - `docker pull nodesource/precise:0.10.37`
  * Node 0.10.38 - `docker pull nodesource/precise:0.10.38`
  * Node 0.10.39 - `docker pull nodesource/precise:0.10.39`
  * Node 0.10.40 - `docker pull nodesource/precise:0.10.40`
  * Node 0.10.41 - `docker pull nodesource/precise:0.10.41`
  * Node 0.12.0 - `docker pull nodesource/precise:0.12.0`
  * Node 0.12.2 - `docker pull nodesource/precise:0.12.2`
  * Node 0.12.3 - `docker pull nodesource/precise:0.12.3`
  * Node 0.12.4 - `docker pull nodesource/precise:0.12.4`
  * Node 0.12.5 - `docker pull nodesource/precise:0.12.5`
  * Node 0.12.6 - `docker pull nodesource/precise:0.12.6`
  * Node 0.12.7 - `docker pull nodesource/precise:0.12.7`
  * Node 0.12.8 - `docker pull nodesource/precise:0.12.8`
  * Node 0.12.9 - `docker pull nodesource/precise:0.12.9`
  * Node 4.1.1 - `docker pull nodesource/precise:4.1.1`
  * Node 4.1.2 - `docker pull nodesource/precise:4.1.2`
  * Node 4.2.0 - `docker pull nodesource/precise:4.2.0`
  * Node 4.2.1 - `docker pull nodesource/precise:4.2.1`
  * Node 4.2.2 - `docker pull nodesource/precise:4.2.2`
  * Node 4.2.3 - `docker pull nodesource/precise:4.2.3`
  * Node 4.2.4 - `docker pull nodesource/precise:4.2.4`
  * Node 4.2.5 - `docker pull nodesource/precise:4.2.5`
  * Node 4.2.6 - `docker pull nodesource/precise:4.2.6`
  * Node 5.0.0 - `docker pull nodesource/precise:5.0.0`
  * Node 5.1.0 - `docker pull nodesource/precise:5.1.0`
  * Node 5.1.1 - `docker pull nodesource/precise:5.1.1`
  * Node 5.2.0 - `docker pull nodesource/precise:5.2.0`
  * Node 5.3.0 - `docker pull nodesource/precise:5.3.0`
  * Node 5.4.0 - `docker pull nodesource/precise:5.4.0`
  * Node 5.4.1 - `docker pull nodesource/precise:5.4.1`
  * Node 5.5.0 - `docker pull nodesource/precise:5.5.0`
* [**Ubuntu trusty**](https://registry.hub.docker.com/u/nodesource/trusty/) - `docker pull nodesource/trusty`
  * Node 0.10.30 - `docker pull nodesource/trusty:0.10.30`
  * Node 0.10.31 - `docker pull nodesource/trusty:0.10.31`
  * Node 0.10.32 - `docker pull nodesource/trusty:0.10.32`
  * Node 0.10.33 - `docker pull nodesource/trusty:0.10.33`
  * Node 0.10.34 - `docker pull nodesource/trusty:0.10.34`
  * Node 0.10.35 - `docker pull nodesource/trusty:0.10.35`
  * Node 0.10.36 - `docker pull nodesource/trusty:0.10.36`
  * Node 0.10.37 - `docker pull nodesource/trusty:0.10.37`
  * Node 0.10.38 - `docker pull nodesource/trusty:0.10.38`
  * Node 0.10.39 - `docker pull nodesource/trusty:0.10.39`
  * Node 0.10.40 - `docker pull nodesource/trusty:0.10.40`
  * Node 0.10.41 - `docker pull nodesource/trusty:0.10.41`
  * Node 0.12.0 - `docker pull nodesource/trusty:0.12.0`
  * Node 0.12.2 - `docker pull nodesource/trusty:0.12.2`
  * Node 0.12.3 - `docker pull nodesource/trusty:0.12.3`
  * Node 0.12.4 - `docker pull nodesource/trusty:0.12.4`
  * Node 0.12.5 - `docker pull nodesource/trusty:0.12.5`
  * Node 0.12.6 - `docker pull nodesource/trusty:0.12.6`
  * Node 0.12.7 - `docker pull nodesource/trusty:0.12.7`
  * Node 0.12.8 - `docker pull nodesource/trusty:0.12.8`
  * Node 0.12.9 - `docker pull nodesource/trusty:0.12.9`
  * Node 4.0.0 - `docker pull nodesource/trusty:4.0.0`
  * Node 4.1.0 - `docker pull nodesource/trusty:4.1.0`
  * Node 4.1.1 - `docker pull nodesource/trusty:4.1.1`
  * Node 4.1.2 - `docker pull nodesource/trusty:4.1.2`
  * Node 4.2.0 - `docker pull nodesource/trusty:4.2.0`
  * Node 4.2.1 - `docker pull nodesource/trusty:4.2.1`
  * Node 4.2.2 - `docker pull nodesource/trusty:4.2.2`
  * Node 4.2.3 - `docker pull nodesource/trusty:4.2.3`
  * Node 4.2.4 - `docker pull nodesource/trusty:4.2.4`
  * Node 4.2.5 - `docker pull nodesource/trusty:4.2.5`
  * Node 4.2.6 - `docker pull nodesource/trusty:4.2.6`
  * Node 5.0.0 - `docker pull nodesource/trusty:5.0.0`
  * Node 5.1.0 - `docker pull nodesource/trusty:5.1.0`
  * Node 5.1.1 - `docker pull nodesource/trusty:5.1.1`
  * Node 5.2.0 - `docker pull nodesource/trusty:5.2.0`
  * Node 5.3.0 - `docker pull nodesource/trusty:5.3.0`
  * Node 5.4.0 - `docker pull nodesource/trusty:5.4.0`
  * Node 5.4.1 - `docker pull nodesource/trusty:5.4.1`
  * Node 5.5.0 - `docker pull nodesource/trusty:5.5.0`
  * iojs 1.3.0 - `docker pull nodesource/trusty:iojs-1.3.0`
  * iojs 1.4.1 - `docker pull nodesource/trusty:iojs-1.4.1`
  * iojs 1.4.2 - `docker pull nodesource/trusty:iojs-1.4.2`
  * iojs 1.4.3 - `docker pull nodesource/trusty:iojs-1.4.3`
  * iojs 1.5.0 - `docker pull nodesource/trusty:iojs-1.5.0`
  * iojs 1.5.1 - `docker pull nodesource/trusty:iojs-1.5.1`
  * iojs 1.6.1 - `docker pull nodesource/trusty:iojs-1.6.1`
  * iojs 1.6.2 - `docker pull nodesource/trusty:iojs-1.6.2`
  * iojs 1.6.3 - `docker pull nodesource/trusty:iojs-1.6.3`
  * iojs 1.6.4 - `docker pull nodesource/trusty:iojs-1.6.4`
  * iojs 1.7.1 - `docker pull nodesource/trusty:iojs-1.7.1`
  * iojs 1.8.1 - `docker pull nodesource/trusty:iojs-1.8.1`
  * iojs 1.8.3 - `docker pull nodesource/trusty:iojs-1.8.3`
  * iojs 1.8.4 - `docker pull nodesource/trusty:iojs-1.8.4`
  * iojs 2.0.0 - `docker pull nodesource/trusty:iojs-2.0.0`
  * iojs 2.0.1 - `docker pull nodesource/trusty:iojs-2.0.1`
  * iojs 2.0.2 - `docker pull nodesource/trusty:iojs-2.0.2`
  * iojs 2.1.0 - `docker pull nodesource/trusty:iojs-2.1.0`
  * iojs 2.2.1 - `docker pull nodesource/trusty:iojs-2.2.1`
  * iojs 2.3.0 - `docker pull nodesource/trusty:iojs-2.3.0`
  * iojs 2.3.1 - `docker pull nodesource/trusty:iojs-2.3.1`
  * iojs 2.3.2 - `docker pull nodesource/trusty:iojs-2.3.2`
  * iojs 2.3.3 - `docker pull nodesource/trusty:iojs-2.3.3`
  * iojs 2.3.4 - `docker pull nodesource/trusty:iojs-2.3.4`
  * iojs 2.4.0 - `docker pull nodesource/trusty:iojs-2.4.0`
  * iojs 2.5.0 - `docker pull nodesource/trusty:iojs-2.5.0`
  * iojs 3.0.0 - `docker pull nodesource/trusty:iojs-3.0.0`
  * iojs 3.1.0 - `docker pull nodesource/trusty:iojs-3.1.0`
  * iojs 3.2.0 - `docker pull nodesource/trusty:iojs-3.2.0`
  * iojs 3.3.0 - `docker pull nodesource/trusty:iojs-3.3.0`
* [**Ubuntu vivid**](https://registry.hub.docker.com/u/nodesource/vivid/) - `docker pull nodesource/vivid`
  * Node 0.10.38 - `docker pull nodesource/vivid:0.10.38`
  * Node 0.10.39 - `docker pull nodesource/vivid:0.10.39`
  * Node 0.10.40 - `docker pull nodesource/vivid:0.10.40`
  * Node 0.10.41 - `docker pull nodesource/vivid:0.10.41`
  * Node 0.12.2 - `docker pull nodesource/vivid:0.12.2`
  * Node 0.12.3 - `docker pull nodesource/vivid:0.12.3`
  * Node 0.12.4 - `docker pull nodesource/vivid:0.12.4`
  * Node 0.12.5 - `docker pull nodesource/vivid:0.12.5`
  * Node 0.12.6 - `docker pull nodesource/vivid:0.12.6`
  * Node 0.12.7 - `docker pull nodesource/vivid:0.12.7`
  * Node 0.12.8 - `docker pull nodesource/vivid:0.12.8`
  * Node 0.12.9 - `docker pull nodesource/vivid:0.12.9`
  * Node 4.0.0 - `docker pull nodesource/vivid:4.0.0`
  * Node 4.1.0 - `docker pull nodesource/vivid:4.1.0`
  * Node 4.1.1 - `docker pull nodesource/vivid:4.1.1`
  * Node 4.1.2 - `docker pull nodesource/vivid:4.1.2`
  * Node 4.2.0 - `docker pull nodesource/vivid:4.2.0`
  * Node 4.2.1 - `docker pull nodesource/vivid:4.2.1`
  * Node 4.2.2 - `docker pull nodesource/vivid:4.2.2`
  * Node 4.2.3 - `docker pull nodesource/vivid:4.2.3`
  * Node 4.2.4 - `docker pull nodesource/vivid:4.2.4`
  * Node 4.2.5 - `docker pull nodesource/vivid:4.2.5`
  * Node 4.2.6 - `docker pull nodesource/vivid:4.2.6`
  * Node 5.0.0 - `docker pull nodesource/vivid:5.0.0`
  * Node 5.1.0 - `docker pull nodesource/vivid:5.1.0`
  * Node 5.1.1 - `docker pull nodesource/vivid:5.1.1`
  * Node 5.2.0 - `docker pull nodesource/vivid:5.2.0`
  * Node 5.3.0 - `docker pull nodesource/vivid:5.3.0`
  * Node 5.4.0 - `docker pull nodesource/vivid:5.4.0`
  * Node 5.4.1 - `docker pull nodesource/vivid:5.4.1`
  * Node 5.5.0 - `docker pull nodesource/vivid:5.5.0`
  * iojs 1.8.1 - `docker pull nodesource/vivid:iojs-1.8.1`
  * iojs 1.8.3 - `docker pull nodesource/vivid:iojs-1.8.3`
  * iojs 1.8.4 - `docker pull nodesource/vivid:iojs-1.8.4`
  * iojs 2.0.0 - `docker pull nodesource/vivid:iojs-2.0.0`
  * iojs 2.0.1 - `docker pull nodesource/vivid:iojs-2.0.1`
  * iojs 2.0.2 - `docker pull nodesource/vivid:iojs-2.0.2`
  * iojs 2.1.0 - `docker pull nodesource/vivid:iojs-2.1.0`
  * iojs 2.2.1 - `docker pull nodesource/vivid:iojs-2.2.1`
  * iojs 2.3.0 - `docker pull nodesource/vivid:iojs-2.3.0`
  * iojs 2.3.1 - `docker pull nodesource/vivid:iojs-2.3.1`
  * iojs 2.3.2 - `docker pull nodesource/vivid:iojs-2.3.2`
  * iojs 2.3.3 - `docker pull nodesource/vivid:iojs-2.3.3`
  * iojs 2.3.4 - `docker pull nodesource/vivid:iojs-2.3.4`
  * iojs 2.4.0 - `docker pull nodesource/vivid:iojs-2.4.0`
  * iojs 2.5.0 - `docker pull nodesource/vivid:iojs-2.5.0`
  * iojs 3.0.0 - `docker pull nodesource/vivid:iojs-3.0.0`
  * iojs 3.1.0 - `docker pull nodesource/vivid:iojs-3.1.0`
  * iojs 3.2.0 - `docker pull nodesource/vivid:iojs-3.2.0`
  * iojs 3.3.0 - `docker pull nodesource/vivid:iojs-3.3.0`

## Centos-based images

* [**Centos 5**](https://registry.hub.docker.com/u/nodesource/centos5/) - `docker pull nodesource/centos5`
  * Node 0.10.31 - `docker pull nodesource/centos5:0.10.31`
  * Node 0.10.32 - `docker pull nodesource/centos5:0.10.32`
  * Node 0.10.33 - `docker pull nodesource/centos5:0.10.33`
  * Node 0.10.34 - `docker pull nodesource/centos5:0.10.34`
  * Node 0.10.35 - `docker pull nodesource/centos5:0.10.35`
  * Node 0.10.36 - `docker pull nodesource/centos5:0.10.36`
  * Node 0.10.38 - `docker pull nodesource/centos5:0.10.38`
  * Node 0.10.39 - `docker pull nodesource/centos5:0.10.39`
  * Node 0.10.40 - `docker pull nodesource/centos5:0.10.40`
  * Node 0.10.41 - `docker pull nodesource/centos5:0.10.41`
* [**Centos 6**](https://registry.hub.docker.com/u/nodesource/centos6/) - `docker pull nodesource/centos6`
  * Node 0.10.31 - `docker pull nodesource/centos6:0.10.31`
  * Node 0.10.32 - `docker pull nodesource/centos6:0.10.32`
  * Node 0.10.33 - `docker pull nodesource/centos6:0.10.33`
  * Node 0.10.34 - `docker pull nodesource/centos6:0.10.34`
  * Node 0.10.35 - `docker pull nodesource/centos6:0.10.35`
  * Node 0.10.36 - `docker pull nodesource/centos6:0.10.36`
  * Node 0.10.38 - `docker pull nodesource/centos6:0.10.38`
  * Node 0.10.39 - `docker pull nodesource/centos6:0.10.39`
  * Node 0.10.40 - `docker pull nodesource/centos6:0.10.40`
  * Node 0.10.41 - `docker pull nodesource/centos6:0.10.41`
  * Node 0.12.1 - `docker pull nodesource/centos6:0.12.1`
  * Node 0.12.2 - `docker pull nodesource/centos6:0.12.2`
  * Node 0.12.3 - `docker pull nodesource/centos6:0.12.3`
  * Node 0.12.5 - `docker pull nodesource/centos6:0.12.5`
  * Node 0.12.6 - `docker pull nodesource/centos6:0.12.6`
  * Node 0.12.7 - `docker pull nodesource/centos6:0.12.7`
  * Node 0.12.8 - `docker pull nodesource/centos6:0.12.8`
  * Node 0.12.9 - `docker pull nodesource/centos6:0.12.9`
* [**Centos 7**](https://registry.hub.docker.com/u/nodesource/centos7/) - `docker pull nodesource/centos7`
  * Node 0.10.31 - `docker pull nodesource/centos7:0.10.31`
  * Node 0.10.32 - `docker pull nodesource/centos7:0.10.32`
  * Node 0.10.33 - `docker pull nodesource/centos7:0.10.33`
  * Node 0.10.34 - `docker pull nodesource/centos7:0.10.34`
  * Node 0.10.35 - `docker pull nodesource/centos7:0.10.35`
  * Node 0.10.36 - `docker pull nodesource/centos7:0.10.36`
  * Node 0.10.38 - `docker pull nodesource/centos7:0.10.38`
  * Node 0.10.39 - `docker pull nodesource/centos7:0.10.39`
  * Node 0.10.40 - `docker pull nodesource/centos7:0.10.40`
  * Node 0.10.41 - `docker pull nodesource/centos7:0.10.41`
  * Node 0.12.1 - `docker pull nodesource/centos7:0.12.1`
  * Node 0.12.2 - `docker pull nodesource/centos7:0.12.2`
  * Node 0.12.3 - `docker pull nodesource/centos7:0.12.3`
  * Node 0.12.5 - `docker pull nodesource/centos7:0.12.5`
  * Node 0.12.6 - `docker pull nodesource/centos7:0.12.6`
  * Node 0.12.7 - `docker pull nodesource/centos7:0.12.7`
  * Node 0.12.8 - `docker pull nodesource/centos7:0.12.8`
  * Node 0.12.9 - `docker pull nodesource/centos7:0.12.9`
  * Node 4.0.0 - `docker pull nodesource/centos7:4.0.0`
  * Node 4.1.0 - `docker pull nodesource/centos7:4.1.0`
  * Node 4.1.1 - `docker pull nodesource/centos7:4.1.1`
  * Node 4.1.2 - `docker pull nodesource/centos7:4.1.2`
  * Node 4.2.0 - `docker pull nodesource/centos7:4.2.0`
  * Node 4.2.1 - `docker pull nodesource/centos7:4.2.1`
  * Node 4.2.2 - `docker pull nodesource/centos7:4.2.2`
  * Node 4.2.3 - `docker pull nodesource/centos7:4.2.3`
  * Node 4.2.4 - `docker pull nodesource/centos7:4.2.4`
  * Node 4.2.5 - `docker pull nodesource/centos7:4.2.5`
  * Node 4.2.6 - `docker pull nodesource/centos7:4.2.6`
  * Node 5.0.0 - `docker pull nodesource/centos7:5.0.0`
  * Node 5.1.0 - `docker pull nodesource/centos7:5.1.0`
  * Node 5.1.1 - `docker pull nodesource/centos7:5.1.1`
  * Node 5.2.0 - `docker pull nodesource/centos7:5.2.0`
  * Node 5.3.0 - `docker pull nodesource/centos7:5.3.0`
  * Node 5.4.0 - `docker pull nodesource/centos7:5.4.0`
  * Node 5.4.1 - `docker pull nodesource/centos7:5.4.1`
  * Node 5.5.0 - `docker pull nodesource/centos7:5.5.0`
  * iojs 2.3.2 - `docker pull nodesource/centos7:iojs-2.3.2`
  * iojs 2.3.3 - `docker pull nodesource/centos7:iojs-2.3.3`
  * iojs 2.3.4 - `docker pull nodesource/centos7:iojs-2.3.4`
  * iojs 2.4.0 - `docker pull nodesource/centos7:iojs-2.4.0`
  * iojs 2.5.0 - `docker pull nodesource/centos7:iojs-2.5.0`
  * iojs 3.0.0 - `docker pull nodesource/centos7:iojs-3.0.0`
  * iojs 3.1.0 - `docker pull nodesource/centos7:iojs-3.1.0`
  * iojs 3.2.0 - `docker pull nodesource/centos7:iojs-3.2.0`
  * iojs 3.3.0 - `docker pull nodesource/centos7:iojs-3.3.0`

## Fedora-based images

* [**Fedora 20**](https://registry.hub.docker.com/u/nodesource/fedora20/) - `docker pull nodesource/fedora20`
  * Node 0.10.31 - `docker pull nodesource/fedora20:0.10.31`
  * Node 0.10.32 - `docker pull nodesource/fedora20:0.10.32`
  * Node 0.10.33 - `docker pull nodesource/fedora20:0.10.33`
  * Node 0.10.34 - `docker pull nodesource/fedora20:0.10.34`
  * Node 0.10.35 - `docker pull nodesource/fedora20:0.10.35`
  * Node 0.10.36 - `docker pull nodesource/fedora20:0.10.36`
  * Node 0.10.38 - `docker pull nodesource/fedora20:0.10.38`
  * Node 0.10.39 - `docker pull nodesource/fedora20:0.10.39`
  * Node 0.10.40 - `docker pull nodesource/fedora20:0.10.40`
  * Node 0.12.1 - `docker pull nodesource/fedora20:0.12.1`
  * Node 0.12.2 - `docker pull nodesource/fedora20:0.12.2`
  * Node 0.12.3 - `docker pull nodesource/fedora20:0.12.3`
  * Node 0.12.5 - `docker pull nodesource/fedora20:0.12.5`
  * Node 0.12.6 - `docker pull nodesource/fedora20:0.12.6`
  * Node 0.12.7 - `docker pull nodesource/fedora20:0.12.7`
  * Node 4.0.0 - `docker pull nodesource/fedora20:4.0.0`
  * Node 4.1.0 - `docker pull nodesource/fedora20:4.1.0`
  * Node 4.1.1 - `docker pull nodesource/fedora20:4.1.1`
  * Node 4.1.2 - `docker pull nodesource/fedora20:4.1.2`
  * Node 4.2.0 - `docker pull nodesource/fedora20:4.2.0`
  * Node 4.2.1 - `docker pull nodesource/fedora20:4.2.1`
  * iojs 2.3.2 - `docker pull nodesource/fedora20:iojs-2.3.2`
  * iojs 2.3.3 - `docker pull nodesource/fedora20:iojs-2.3.3`
  * iojs 2.3.4 - `docker pull nodesource/fedora20:iojs-2.3.4`
  * iojs 2.4.0 - `docker pull nodesource/fedora20:iojs-2.4.0`
  * iojs 2.5.0 - `docker pull nodesource/fedora20:iojs-2.5.0`
  * iojs 3.0.0 - `docker pull nodesource/fedora20:iojs-3.0.0`
  * iojs 3.1.0 - `docker pull nodesource/fedora20:iojs-3.1.0`
  * iojs 3.2.0 - `docker pull nodesource/fedora20:iojs-3.2.0`
  * iojs 3.3.0 - `docker pull nodesource/fedora20:iojs-3.3.0`
* [**Fedora 21**](https://registry.hub.docker.com/u/nodesource/fedora21/) - `docker pull nodesource/fedora21`
  * Node 0.10.35 - `docker pull nodesource/fedora21:0.10.35`
  * Node 0.10.36 - `docker pull nodesource/fedora21:0.10.36`
  * Node 0.10.38 - `docker pull nodesource/fedora21:0.10.38`
  * Node 0.10.39 - `docker pull nodesource/fedora21:0.10.39`
  * Node 0.10.40 - `docker pull nodesource/fedora21:0.10.40`
  * Node 0.10.41 - `docker pull nodesource/fedora21:0.10.41`
  * Node 0.12.1 - `docker pull nodesource/fedora21:0.12.1`
  * Node 0.12.2 - `docker pull nodesource/fedora21:0.12.2`
  * Node 0.12.3 - `docker pull nodesource/fedora21:0.12.3`
  * Node 0.12.5 - `docker pull nodesource/fedora21:0.12.5`
  * Node 0.12.6 - `docker pull nodesource/fedora21:0.12.6`
  * Node 0.12.7 - `docker pull nodesource/fedora21:0.12.7`
  * Node 0.12.8 - `docker pull nodesource/fedora21:0.12.8`
  * Node 0.12.9 - `docker pull nodesource/fedora21:0.12.9`
  * Node 4.0.0 - `docker pull nodesource/fedora21:4.0.0`
  * Node 4.1.0 - `docker pull nodesource/fedora21:4.1.0`
  * Node 4.1.1 - `docker pull nodesource/fedora21:4.1.1`
  * Node 4.1.2 - `docker pull nodesource/fedora21:4.1.2`
  * Node 4.2.0 - `docker pull nodesource/fedora21:4.2.0`
  * Node 4.2.1 - `docker pull nodesource/fedora21:4.2.1`
  * Node 4.2.2 - `docker pull nodesource/fedora21:4.2.2`
  * Node 4.2.3 - `docker pull nodesource/fedora21:4.2.3`
  * Node 4.2.4 - `docker pull nodesource/fedora21:4.2.4`
  * Node 4.2.5 - `docker pull nodesource/fedora21:4.2.5`
  * Node 4.2.6 - `docker pull nodesource/fedora21:4.2.6`
  * Node 5.0.0 - `docker pull nodesource/fedora21:5.0.0`
  * Node 5.1.0 - `docker pull nodesource/fedora21:5.1.0`
  * Node 5.1.1 - `docker pull nodesource/fedora21:5.1.1`
  * Node 5.2.0 - `docker pull nodesource/fedora21:5.2.0`
  * Node 5.3.0 - `docker pull nodesource/fedora21:5.3.0`
  * Node 5.4.0 - `docker pull nodesource/fedora21:5.4.0`
  * Node 5.4.1 - `docker pull nodesource/fedora21:5.4.1`
  * Node 5.5.0 - `docker pull nodesource/fedora21:5.5.0`
  * iojs 2.3.2 - `docker pull nodesource/fedora21:iojs-2.3.2`
  * iojs 2.3.3 - `docker pull nodesource/fedora21:iojs-2.3.3`
  * iojs 2.3.4 - `docker pull nodesource/fedora21:iojs-2.3.4`
  * iojs 2.4.0 - `docker pull nodesource/fedora21:iojs-2.4.0`
  * iojs 2.5.0 - `docker pull nodesource/fedora21:iojs-2.5.0`
  * iojs 3.0.0 - `docker pull nodesource/fedora21:iojs-3.0.0`
  * iojs 3.1.0 - `docker pull nodesource/fedora21:iojs-3.1.0`
  * iojs 3.2.0 - `docker pull nodesource/fedora21:iojs-3.2.0`
  * iojs 3.3.0 - `docker pull nodesource/fedora21:iojs-3.3.0`
* [**Fedora 22**](https://registry.hub.docker.com/u/nodesource/fedora22/) - `docker pull nodesource/fedora22`
  * Node 0.10.40 - `docker pull nodesource/fedora22:0.10.40`
  * Node 0.10.41 - `docker pull nodesource/fedora22:0.10.41`
  * Node 4.0.0 - `docker pull nodesource/fedora22:4.0.0`
  * Node 4.1.0 - `docker pull nodesource/fedora22:4.1.0`
  * Node 4.1.1 - `docker pull nodesource/fedora22:4.1.1`
  * Node 4.1.2 - `docker pull nodesource/fedora22:4.1.2`
  * Node 4.2.0 - `docker pull nodesource/fedora22:4.2.0`
  * Node 4.2.1 - `docker pull nodesource/fedora22:4.2.1`
  * Node 4.2.2 - `docker pull nodesource/fedora22:4.2.2`
  * Node 4.2.3 - `docker pull nodesource/fedora22:4.2.3`
  * Node 4.2.4 - `docker pull nodesource/fedora22:4.2.4`
  * Node 4.2.5 - `docker pull nodesource/fedora22:4.2.5`
  * Node 4.2.6 - `docker pull nodesource/fedora22:4.2.6`
  * Node 5.0.0 - `docker pull nodesource/fedora22:5.0.0`
  * Node 5.1.0 - `docker pull nodesource/fedora22:5.1.0`
  * Node 5.1.1 - `docker pull nodesource/fedora22:5.1.1`
  * Node 5.2.0 - `docker pull nodesource/fedora22:5.2.0`
  * Node 5.3.0 - `docker pull nodesource/fedora22:5.3.0`
  * Node 5.4.0 - `docker pull nodesource/fedora22:5.4.0`
  * Node 5.4.1 - `docker pull nodesource/fedora22:5.4.1`
  * Node 5.5.0 - `docker pull nodesource/fedora22:5.5.0`

# Contributing

To submit a bug report, please create an [issue at GitHub][https://github.com/nodesource/docker-node/issues/new].

If you'd like to contribute code to this project, please read the
[CONTRIBUTING.md][https://github.com/nodesource/docker-node/blob/master/CONTRIBUTING.md] document.

# Authors and Contributors

<table><tbody>
  <tr>
    <th align="left">William Blankenship</th>
    <td><a href="https://github.com/retrohacker">GitHub/retrohacker</a></td>
    <td><a href="https://twitter.com/retrohack3r">Twitter/@retrohack3r</a></td>
  </tr>
</tbody></table>

# License & Copyright

**docker-node** is Copyright (c) 2016 NodeSource and licensed under the
MIT license. All rights not explicitly granted in the MIT license are reserved.
See the included [LICENSE.md][https://github.com/nodesource/docker-node/blob/master/LICENSE.md] file for more details.
