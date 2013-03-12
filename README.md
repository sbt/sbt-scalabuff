# sbt-scalabuff

[SBT](http://github.com/harrah/xsbt) plugin to generate scala case class from [Google Protocol Buffers](https://developers.google.com/protocol-buffers/) using [ScalaBuff](https://github.com/SandroGrzicic/ScalaBuff).

## Usage

Adding the plugin:

    addSbtPlugin("com.github.sbt" %% "sbt-scalabuff" % "0.2")

Enable the plugin in your build:

    import scalabuff.ScalaBuffPlugin._

    object build extends Build {
      lazy val root = Project("main", file("."), settings = Defaults.defaultSettings ++ scalaBuffSettings).configs(ScalaBuff)
    }

Once activated place your '.proto' definition in *src/main/protobuf* and that's all!

## Contribution Policy

Contributions via GitHub pull requests are gladly accepted from their original author.
Along with any pull requests, please state that the contribution is your original work and 
that you license the work to the project under the project's open source license.
Whether or not you state this explicitly, by submitting any copyrighted material via pull request, 
email, or other means you agree to license the material under the project's open source license and 
warrant that you have the legal authority to do so.

## License

    This software is licensed under the Apache 2 license, quoted below.

    Copyright 2009-2013 Alois Cochard 

    Licensed under the Apache License, Version 2.0 (the "License"); you may not
    use this file except in compliance with the License. You may obtain a copy of
    the License at http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
    WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
    License for the specific language governing permissions and limitations under
    the License.
