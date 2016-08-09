# tensorcat

```julia
$ julia
               _
   _       _ _(_)_     |  A fresh approach to technical computing
  (_)     | (_) (_)    |  Documentation: http://docs.julialang.org
   _ _   _| |_  __ _   |  Type "?help" for help.
  | | | | | | |/ _` |  |
  | | |_| | | | (_| |  |  Version 0.6.0-dev.100 (2016-08-08 21:35 UTC)
 _/ |\__'_|_|_|\__'_|  |  Commit 2037464* (0 days old master)
|__/                   |  x86_64-apple-darwin16.0.0

julia> Pkg.checkout("TensorFlow")
```

```julia
julia> using PyCall

julia> @pyimport tensorflow as tf

julia> hello = tf.constant("Hello, TensorFlow!")
PyObject <tf.Tensor 'Const:0' shape=() dtype=string>

julia> sess = tf.Session()
PyObject <tensorflow.python.client.session.Session object at 0x31a277190>

julia> result = sess[:run](hello)
"Hello, TensorFlow!"

julia> a = tf.constant(10)
PyObject <tf.Tensor 'Const_1:0' shape=() dtype=int32>

julia> b = tf.constant(32)
PyObject <tf.Tensor 'Const_2:0' shape=() dtype=int32>

julia> result = sess[:run](a[:__add__](b))
0-dimensional Array{Int32,0}:
42
```
