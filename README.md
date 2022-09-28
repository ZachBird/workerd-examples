<h1 align="center"><samp>Workerd Examples</samp></h1>

#### binary build from 
https://github.com/cloudflare/workerd

#### example from 
https://github.com/cloudflare/workerd/tree/main/samples

#### usage

# Hello World Example

To run the example on http://localhost:8888

configuration of example is in **config.capnp** file

```sh
$ ../bin/workerd serve config.capnp
```

To run using bazel

```sh
$ bazel run //src/workerd/server:workerd -- serve ~/cloudflare/workerd/samples/helloworld/config.capnp
```

To create a standalone binary that can be run:

```sh
$ ../bin/workerd compile config.capnp > helloworld

$ ./helloworld
```

To test:

```sh
% curl http://localhost:8888
Hello World
```