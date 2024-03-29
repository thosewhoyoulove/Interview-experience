<!--
 * @Description:
 * @Author: 曹俊
 * @Date: 2022-11-11 20:23:31
 * @LastEditors: 曹俊
 * @LastEditTime: 2023-03-27 14:51:13
-->

# 自我介绍
面试官你好，我叫曹俊，是一名来自湖南科技大学计算机科学与工程学院物联网工程专业的一名大四学生，在大学期间，无挂科，绩点3.0左右，有拿过奖学金以及校级奖励，主要实习经历是在学校的网络信息中心实习，在里面担任的是一名前端开发工程师，主要项目经验有实习期间的面对面签到系统以及阳光服务平台，其余的都是自己做的项目，有一个基于网易开放平台的云音乐移动端网页，项目是从0到1开发，并部署到服务器上实现在线访问，另一个是一个文件解析网页，能够将特定的docx文件解析为指定样式的网页，供二次使用，并部署到GitHub pages上支持在线访问


## 在Vue中优化大数据量的页面渲染主要有以下几个方面：

- 使用虚拟列表或者虚拟滚动等技术，只渲染可见区域内的数据。通过监听滚动事件并计算当前可见区域动态生成DOM节点，可以大大减少不必要的DOM节点渲染和计算，从而提升渲染效率。Vue 的第三方插件 vue-virtual-scroll-list 和 vue-virtual-scroll-tree 提供了常见的虚拟列表和虚拟树组件。

- 利用Vue的computed计算属性实现数据格式转换和缓存。通过将大量的数据转换为Vue的响应式计算属性，可以减少重复渲染和计算，提升性能。在数据源更新时，Vue只会计算变更的部分和相关依赖，并实时更新渲染结果。

- 合理使用Vue的v-if和v-for等指令来避免不必要的DOM元素渲染。除了虚拟列表等技术外，Vue也提供了一些指令来动态处理DOM元素的显隐和数据绑定。通过结合v-if和v-for等指令，可以避免不必要的DOM元素渲染，减少渲染负担。

## 对前端工程化的理解：
#### 前端工程化是一种利用工具和流程优化前端开发流程的方法，旨在提高项目的可维护性、可扩展性和可复用性。它主要包括以下几个方面：

- 模块化开发：模块化开发可以将复杂的代码分解成更小的、独立的模块，提高代码的可维护性和可复用性。

- 自动化构建：自动化构建可以自动处理前端代码的编译、压缩、合并等工作，提高开发效率和代码质量。

- 自动化测试：自动化测试可以自动运行测试用例，通过自动化的测试流程，可以减少手动测试的工作量，同时保证代码质量和稳定性。

- 版本控制：版本控制可以记录代码的变化历史和归档备份，帮助开发者随时追踪代码的变化历史和进行协同开发。

- 持续集成：持续集成可以通过自动化的方式不断集成和测试代码的更新，从而提供更加及时的反馈和更高的代码质量。

#### 综上所述，前端工程化是一种将前端开发流程自动化、标准化的方法，能够提高开发效率、代码质量和团队协作能力。




## 前端常见的安全问题包括：

- XSS攻击（Cross Site Scripting）：通过注入恶意脚本来控制网页展示内容，窃取用户数据。

- CSRF攻击（Cross-Site Request Forgery）：攻击者通过欺骗用户发出伪造的请求，在用户不知情的情况下，偷偷攻击已登陆的网站。


#### 针对这些安全问题，可以采取以下对策：

- XSS攻击对策：对用户输入进行过滤和转义，过滤掉危险的字符和标签;使用 HttpOnly 属性限制 cookie 只能在 HTTP 请求中传输，防止 cookie 被窃取;使用 CSP（Content Security Policy是一项安全策略，它可以帮助网站防止 XSS、点击劫持等攻击，通过指定允许加载的资源，限制网页中脚本的执行，从而提高网站的安全性。）限制网页中脚本的执行，只允许加载指定的脚本资源;对 URL 参数进行校验和过滤，防止恶意脚本的注入。

- CSRF 攻击对策：验证来源站点：服务器端可以对请求来源站点进行验证，只接受来自合法站点的请求;随机 token：服务器端可以在用户登录时生成一个随机 token，并在每次表单提交时验证 token 的有效性;双重认证：服务器端可以采用双重认证，例如使用短信或者邮箱验证码等方式，增加攻击者的攻击难度;双重认证：服务器端可以采用双重认证，例如使用短信或者邮箱验证码等方式，增加攻击者的攻击难度。

## HTTP 和 HTTPS 之间的主要区别是：

- 安全性：HTTPS 比 HTTP 更加安全。HTTPS 使用 SSL（Secure Sockets Layer）或 TLS（Transport Layer Security）加密协议来确保数据传输的安全性，加密后的数据不容易被窃听或篡改。

- 端口号：HTTP 使用 80 端口，HTTPS 使用 443 端口。这是为了防止在传输过程中发生端口冲突。

- 证书：为了使用 HTTPS，需要使用数字证书来验证网站的身份。数字证书由受信任的第三方颁发机构（CA）颁发，用于证明网站的身份和安全性。在 HTTPS 连接中，浏览器会验证数字证书，如果验证通过，则建立安全连接；如果验证失败，则会弹出警告信息。

- 性能：HTTPS 在建立连接时需要进行 SSL/TLS 握手，这可能会导致一些连接和传输的性能损失。但是，随着计算机和服务器硬件的不断升级，这种影响已经被大大降低，因此，在安全性和性能之间进行权衡是非常值得的。

#### 综上所述，HTTPS 更加安全，但在某些情况下可能会影响性能。因此，选择使用哪种协议取决于应用的性质和特定的需求。

## HTTP/1.1 相比 HTTP/1.0 提高了以下性能：
- 持久连接 (Persistent Connections) : HTTP/1.1默认启用了持久连接：connection：Keep-Alive，意味着一个TCP连接可以被用来传输多个请求和响应，而不必每次都建立和断开连接，减少了频繁地创建和关闭连接，节省了不必要的时间和带宽消耗。
- 支持管道（pipeline）传输：允许客户端同时发送多个请求给服务器，而且不必等待服务器响应就能发送下一个请求。这个特性可以有效减少网络延迟，从而提高页面加载速度。
- 增加了缓存管理 (Caching) : HTTP/1.1增加了缓存控制（Cache Control）和实体标签（Entity Tags）等功能，支持更高效的缓存机制，减少了服务器端和客户端的通信次数，增加了服务器和客户端的性能指标。
- 虚拟主机 (Virtual Hosting) : HTTP/1.1通过引入Host头来实现虚拟主机管理，允许多个域名指向同一IP地址的不同Web服务器，节省了服务器资源，并且可以提高对多个域名的支持。
- 块编码传输（chunked Transfer Encoding）：HTTP/1.1还引入了块编码传输，可以将数据分块传输。这个特性可以更好地支持流媒体等非标准的内容传输方式。

## HTTP/2.0 相比于 HTTP/1.1 提高了以下性能：

- 多路复用：HTTP/2.0 使用二进制分帧，可以在同一个连接上同时传输多个请求和响应，避免了 HTTP/1.1 中的队头阻塞问题，提高了并发性能和响应速度。

- 二进制分帧：HTTP/2.0 将请求和响应拆分成二进制的帧，每个帧都有自己的标识符，可以被无序地发送和接收，避免了 HTTP/1.1 中的序列化和阻塞问题，提高了传输效率和传输速度。

- 首部压缩：HTTP/2.0 使用 HPACK 算法对 HTTP 首部进行压缩，减少了网络传输的数据量，提高了传输效率和传输速度。

- 服务器推送：HTTP/2.0 允许服务器在客户端请求之前主动向客户端推送资源，避免了客户端请求资源的延迟，提高了性能和响应速度。

- 流量控制：HTTP/2.0 支持流级别的流量控制，可以动态地控制流的数据传输速度，避免了网络拥塞和过载问题，提高了传输效率和传输速度。
## Get和Post方法的区别

#### Get和Post是HTTP协议中常用的两种请求方法，它们的主要区别在于：

- 语义不同：GET方法用于请求获取资源，而POST方法用于提交资源。

- 传输方式不同：GET方法将请求参数放在URL的查询字符串中传输，而POST方法将请求参数放在请求体中传输。

- 安全性不同：GET方法的请求参数会被明文显示在URL中，安全性较低，而POST方法的请求参数则被包含在请求体中，相对更安全。

- 适用场景不同：GET方法适用于获取资源的场景，如查看文章、浏览图片等，而POST方法适用于提交资源的场景，如提交表单、上传文件等。

- 缓存机制不同：GET方法的响应可以被缓存，而POST方法的响应禁止被缓存。

- 重试机制不同：GET方法是安全的和幂等的，可以重复执行而不会对资源产生影响，而POST方法不是幂等的，重复执行可能会对资源产生影响。
## 浏览器缓存机制
#### 浏览器缓存机制指的是浏览器在访问 Web 页面时，会自动将一些资源缓存到本地，以便下次访问时可以直接从缓存中获取，从而提高页面的加载速度和降低服务器的负载。浏览器缓存机制主要分为强缓存和协商缓存两种方式。

- 使用强缓存策略时，如果缓存资源有效，则直接使用缓存资源，不必再向服务器发起请求。强缓存策略可以通过两种方式来设置，分别是 http 头信息中的 Expires 属性和 Cache-Control 属性。

  - 服务器通过在响应头中添加 `Expires` 属性，来指定资源的过期时间。在过期时间以内，该资源可以被缓存使用，不必再向服务器发送请求。这个时间是一个绝对时间，它是服务器的时间，因此可能存在这样的问题，就是客户端的时间和服务器端的时间不一致，或者用户可以对客户端时间进行修改的情况，这样就可能会影响缓存命中的结果。

  - Expires 是 http1.0 中的方式，因为它的一些缺点，在 http 1.1 中提出了一个新的头部属性就是 `Cache-Control` 属性，它提供了对资源的缓存的更精确的控制。它有很多不同的值，常用的比如我们可以通过设置 max-age 来指定资源能够被缓存的时间的大小，这是一个相对的时间，它会根据这个时间的大小和资源第一次请求时的时间来计算出资源过期的时间，因此相对于 Expires 来说，这种方式更加有效一些。常用的还有比如 private ，用来规定资源只能被客户端缓存，不能够代理服务器所缓存。还有如 no-store ，用来指定资源不能够被缓存，no-cache 代表该资源能够被缓存，但是立即失效，每次都需要向服务器发起请求。

#### 一般来说只需要设置其中一种方式就可以实现强缓存策略，当两种方式一起使用时，Cache-Control 的优先级要高于 Expires 。


- 使用协商缓存策略时，会先向服务器发送一个请求，如果资源没有发生修改，则返回一个 304 状态，让浏览器使用本地的缓存副本。如果资源发生了修改，则返回修改后的资源。协商缓存也可以通过两种方式来设置，分别是 http 头信息中的 `Etag` 和 `Last-Modified` 属性。

  - 服务器通过在响应头中添加 `Last-Modified` 属性来指出资源最后一次修改的时间，当浏览器下一次发起请求时，会在请求头中添加一个 `If-Modified-Since` 的属性，属性值为上一次资源返回时的 Last-Modified 的值。当请求发送到服务器后服务器会通过这个属性来和资源的最后一次的修改时间来进行比较，以此来判断资源是否做了修改。如果资源没有修改，那么返回 `304` 状态，让客户端使用本地的缓存。如果资源已经被修改了，则返回修改后的资源。使用这种方法有一个缺点，就是 Last-Modified 标注的最后修改时间只能精确到`秒`级，如果某些文件在 1 秒钟以内，被修改多次的话，那么文件已将改变了但是 `Last-Modified` 却没有改变，这样会造成缓存命中的不准确。

  - 因为 `Last-Modified` 的这种可能发生的不准确性，http 中提供了另外一种方式，那就是 `Etag` 属性。服务器在返回资源的时候，在头信息中添加了 Etag 属性，这个属性是资源生成的`唯一标识符`，当资源发生改变的时候，这个值也会发生改变。在下一次资源请求时，浏览器会在请求头中添加一个 `If-None-Match` 属性，这个属性的值就是上次返回的资源的 `Etag` 的值。服务接收到请求后会根据这个值来和资源当前的 Etag 的值来进行比较，以此来判断资源是否发生改变，是否需要返回资源。通过这种方式，比 Last-Modified 的方式更加精确。


#### 当 Last-Modified 和 Etag 属性同时出现的时候，Etag 的优先级更高。使用协商缓存的时候，服务器需要考虑负载平衡的问题，因此多个服务器上资源的 Last-Modified 应该保持一致，因为每个服务器上 Etag 的值都不一样，因此在考虑负载平衡时，最好不要设置 Etag 属性。

#### 强缓存策略和协商缓存策略在缓存命中时都会直接使用本地的缓存副本，区别只在于协商缓存会向服务器发送一次请求。它们缓存不命中时，都会向服务器发送请求来获取资源。在实际的缓存机制中，强缓存策略和协商缓存策略是一起合作使用的。浏览器首先会根据请求的信息判断，强缓存是否命中，如果命中则直接使用资源。如果不命中则根据头信息向服务器发起请求，使用协商缓存，如果协商缓存命中的话，则服务器不返回资源，浏览器直接使用本地资源的副本，如果协商缓存不命中，则浏览器返回最新的资源给浏览器。

## 什么是 Node.js？
Node.js 是一个使用 JavaScript 语言开发的开源、跨平台的运行时环境，它使得开发者可以在服务器端使用 JavaScript 进行开发。

## Node.js 的优势是什么？

- 事件驱动、非阻塞 I/O 模型；
- 轻量、高效、易于扩展；
- 使用 JavaScript，使得跨平台开发更为便捷。
- Node.js 能够应对哪些类型的任务？
- Node.js 不适合 CPU 密集型任务，但适合处理 I/O 密集型任务，比如网络通信、文件操作等等。

## ES Module（ESM）和CommonJS（CJS）的区别
#### ES Module（ESM）和CommonJS（CJS）都是用于 JavaScript 模块化的规范，用于组织和管理 JavaScript 代码，但它们有以下几点区别：

- 语法不同：ESM采用import和export关键字来定义和导出模块，而CJS采用require和module.exports语法。

- 代码执行时机不同：ESM是在编译时就可以确定，而 CJS 是在运行时确定的，所以如果是在浏览器环境下，需要先下载完整个 JS 文件才能去解析运行。

- 加载方式不同：ESM是静态引入，通过在 HTML 的 module 标签或者 JavaScript 的 import 引入，所以他们能够在浏览器环境下完美地支持懒加载、异步等方式，而CJS是动态引入，只能通过代码的形式在程序运行时动态加载。

- 变量绑定方式不同：ESM可以在导入的模块中，直接引用导出模块的变量，同时包含整个模块的变量，而CJS中所有导入都是传值赋值，导出的值会通过引用传递。

#### 综上所述，ES Module 是 ECMAScript（JavaScript）官方制定的模块化方案，跟浏览器的 ECMAScript 实现结合更紧密；CommonJS 是 Node.js 默认的模块化规范，更适用于服务端，可以动态加载模块并支持模块导入的缓存。


- TypeScript 是什么？它有什么优点？
  TypeScript 是一种由微软开发的静态类型检查的编程语言，它是 JavaScript 的超集，可以编译成纯 JavaScript。TypeScript 有以下优点：

  - 提供了静态类型检查，可以在编译时发现类型错误，减少运行时错误。

  - 支持 ES6+ 的语法，可以使用最新的 JavaScript 特性。

  - 增强了代码可读性和可维护性，可以使用接口、泛型、枚举等特性。

  - 提供了更好的编辑器支持，可以实现智能提示、自动补全等功能。

- TypeScript 中的接口是什么？它有什么作用？
 接口（Interface）是 TypeScript 中的一个重要概念，用于描述对象的形状。可以使用接口来定义对象的属性和方法，从而提高代码可读性和可维护性。例如：
 
```ts
interface Person {
  name: string;
  age: number;
  sayHello: () => void;
}

const person: Person = {
  name: 'Alice',
  age: 20,
  sayHello() {
    console.log(`Hello, my name is ${this.name}.`);
  }
};
```

- TypeScript 中的泛型是什么？它有什么作用？

泛型（Generics）是 TypeScript 中的一个重要特性，可以在定义函数、类、接口等时使用，用于增强代码的复用性和灵活性。泛型可以让函数或类可以接受任意类型的参数，从而实现更加通用的代码。例如：
```ts
function identity<T>(arg: T): T {
  return arg;
}

const result = identity('hello');
```
- TypeScript 中的类是什么？它有什么特点？

  类（Class）是 TypeScript 中的一个重要概念，用于描述面向对象的编程模型。类可以包含属性、方法、构造函数等，可以继承其他类，实现接口等。类的特点包括：

  - 支持公共、私有、受保护和只读的属性。

  - 支持静态属性和静态方法。

  - 支持继承和多态。

  - 支持实现接口。

- TypeScript 中的模块是什么？它有什么作用？

  模块（Module）是 TypeScript 中的一个重要概念，用于组织代码，将代码分割为可重用的单元。模块可以导出和导入变量、类、函数等，从而实现更好的代码可维护性和可复用性。模块的特点包括：

  - 可以将代码分割为多个文件，避免代码冗长和混乱。

  - 可以使用 import 和 export 关键字导入和导出模块。

  - 可以使用命名空间（Namespace）来组织代码。

# Vite 是一个基于 ES modules 的构建工具，它的快速主要有以下几个原因：

- 基于 ES modules：Vite 采用了基于 ES modules 的开发方式，通过浏览器原生支持的模块化加载机制，实现了快速的模块热更新（HMR）。相比传统的构建工具，它不需要打包整个应用，而是只需要在需要更新的模块中进行热更新，从而大大提高了开发效率。

- 预构建：Vite 会在启动时预先构建应用中的所有模块，并将它们缓存到内存中，这样在开发过程中每次需要加载模块时，都可以直接从内存中获取，避免了磁盘读取和网络请求的时间消耗，从而提高了开发效率。

- 插件机制：Vite 提供了强大的插件机制，允许开发者根据自己的需求扩展构建工具的功能，例如支持 TypeScript、CSS 预处理器等。这样可以避免在开发过程中频繁切换工具，提高了开发效率。

- 轻量级：Vite 的设计理念是轻量级，它只关注开发阶段的静态资源加载和模块热更新，不涉及代码压缩、混淆等操作。这样可以避免不必要的性能消耗，从而提高了开发效率。

# Node面试题
## 问题
- 解释一下Node.js及其工作原理。
  -  Node.js是一个基于Chrome V8引擎的服务器端JavaScript运行环境。它采用事件驱动、非阻塞I/O模型，使其轻量、高效并具有良好的可扩展性。Node.js的工作原理是基于事件循环的，这意味着它在执行时将会以异步(callback)的方式处理用户请求。

- Node.js的优缺点是什么？
  -  Node.js的优点包括：高效率、低延迟、轻量、跨平台、良好的可扩展性、清晰的架构等。缺点包括：处理CPU密集型操作和多核处理的能力较弱、对于新手不够友好等。
- 解释一下事件驱动性的编程是什么意思。这对Node.js有什么影响？
  -  事件驱动编程是一种编程理念，通过异步(callback)方式处理用户请求，以最小的时间响应并处理更多的请求。这种编程方式更适用于I/O密集型操作，因为它无需等待系统调用，从而获得更高的并发性和更低的延迟。Node.js就是基于这种事件驱动性编程的方式而设计的。
- 什么是回调函数？在Node.js中，为什么会经常使用它们？
  -  回调函数是将一个函数作为参数传递给另一个函数，并在后者执行后被执行。在Node.js中，由于其异步特性，许多API都是基于回调函数的方式实现，以便在异步操作完成后获得结果。

- 解释一下Node.js中的事件循环是什么。这对Node.js有什么影响。
  - Node.js的事件循环是一个处理器在等待和处理事件消息的过程。它采用单线程模型，但利用事件和非阻塞I/O使单线程能够处理大量的并发连接。事件循环采用异步(callback)的方式处理用户请求，以最小的时间响应并处理更多请求。

- 什么是模块？以及在Node.js中如何使用模块？
  - 在Node.js中，每个文件都被视为一个模块。这使得其易于使用和组织代码。可以通过导出和导入的方式使用模块化的代码。

- 解释一下提高Node.js性能的技术。
  - Node.js提供了一些工具和技术，例如利用cahce加速之前已经加载过的模块、应用性能优化工具如PM2、Node-clinic、应用集群、代码优化等方法来提高Node.js的性能。

- 什么是Promise？解释一下如何在Node.js中使用Promise。
  - Promise是一种解决回调嵌套问题的新式Api，使代码更清晰易懂并更具可读性。在Node.js中，可以利用Promise实现更好的代码维护，避免回调函数过深嵌套的问题。

- 解释一下Node.js中的缓冲区(Buffer)是什么。
  - 缓冲区(Buffer)类似于数组，但也有一些重要的区别。它是一个被优化为处理二进制数的类数组对象。Node.js缓冲区使用在TCP流或文件系统操作等场景中处理数据，每当需要在Stream中传输数据时，就会发生缓冲操作。

- 如何在Node.js中进行调试？
  
  - 在Node.js中，可以使用内置的调试器或者第三方调试工具，例如Chrome DevTools Inspector扩展程序实现。可以通过控制台调用setBreakpoint函数来设置断点，也可以模拟使用Node.js解释器的命令行。

# 对路由原理的理解

## 前端路由是一种用于实现单页面应用（SPA）的技术，它可以在不刷新页面的情况下改变URL并渲染对应的页面内容。

#### 前端路由有两种模式：

- Hash模式：使用URL中的hash（即#号后面的部分）来模拟路由，例如：``http://example.com/#/path/to/page``。当URL中的hash发生变化时，可以使用JavaScript监听hashchange事件并根据hash的值来渲染对应的页面内容。
  - 优点：兼容性好，可以在不支持HTML5 History API的浏览器中使用；
  - 缺点是URL不太美观，且hash值不会被发送到服务器端。

- History模式：使用HTML5 History API中的pushState()和replaceState()方法来改变URL，例如：``http://example.com/path/to/page``。当URL发生变化时，可以使用JavaScript监听popstate事件并根据URL的路径来渲染对应的页面内容。
  - 优点：URL美观且更符合传统的URL风格，可以使用所有HTTP方法（如GET、POST等）；
  - 缺点是需要服务器端的支持，因为URL中的路径会被发送到服务器端，需要在服务器端进行相应的配置。（使用Nginx）

#### 使用Nginx服务配置history模式
#### 在Nginx服务器中，需要在配置文件中添加以下代码：
```nginx
server {
  root /var/www/html;
  index index.html;
  server_name yourdomain.com;

  location / {
    try_files $uri $uri/ /index.html;
  }
}
```

```
这个代码块的作用是，当请求的文件或目录不存在时，将请求都定向到index.html文件。需要注意的是，在配置中需要将yourdomain.com替换为实际的域名或IP地址，并将root指向Vue.js项目的根目录。配置好服务器路由规则后，就可以在Vue.js中使用history模式，而不会出现404错误了。
```
# 对单点登录的理解
## 前端的单点登录（Single Sign-On，简称SSO）通常指的是在多个应用系统中，用户只需要登录一次，就可以访问所有系统的资源，而不需要再次登录。前端实现单点登录常常采用基于 Token 或者 Session 的方式进行身份验证。

#### 简单来说，就是用户在第一次登录认证之后，会在服务器端生成一个授权 Token 或 Session，后续用户在访问其他应用系统时，只需要通过 Token 或 Session 进行身份验证就可以了。

#### 实现前端单点登录的具体步骤包括：

- 用户在第一次登录之后，前端向后端请求认证并获取Token或Session；

- 前端将Token或Session存储在浏览器的Cookie或LocalStorage中；

- 用户访问其他应用系统时，前端将Token或Session发送给后端进行身份验证；

- 后端验证Token或Session的有效性，如果通过验证则返回相应的资源；

- 如果Token或Session过期或者验证失败，用户需要重新进行身份验证。

#### 总之，前端单点登录在多个应用系统中实现用户身份认证的一致性，可以提高用户的使用效率和用户体验。


# Vue中computed和watch的区别

## Vue中computed和watch都是响应式的特性，用于监听数据的变化，但是它们之间具有不同的功能和使用场景。

- Computed：

  - Computed是Vue中用来对数据进行计算和处理的属性。computed属性是基于它们的依赖进行缓存的，也就是说只要它的相关依赖没有发生变化，它就会一直使用缓存的值。Computed只有在依赖的数据发生变化时才会重新计算，因此具有较高性能的特点。

  - 使用场景：当需要对数据进行计算和处理，并且该计算是基于响应式数据的时候，常常使用computed。

- Watch：

  - watch是观察者，Vue通过watch来观察某个数据的变化，并执行相应的回调函数。只要数据发生改变，watch就会执行回调函数。这在需要执行异步或开销较大的操作时非常有用。watch可以监听单个数据，也可以监听表达式，还可以在监听方法中获取新旧的值。

  - 使用场景：当需要在数据变化时，执行一些异步或复杂的操作时，常常使用watch来监听数据的变化。

#### 总结：

- Computed：计算属性，是基于依赖缓存的，只有在依赖发生变化时才会重新计算，适用于计算复杂且对性能要求较高的数据情况。

- Watch：监听数据，只要数据发生变化就会执行回调函数，适用于监听某些值的变化并执行异步或开销较大的操作的情况。

# Document对象和Window对象的区别
### Document对象是当前HTML页面的根节点，它是HTML DOM的一部分，用于访问文档中的所有节点和元素。而Window对象则代表整个浏览器窗口，是BOM（浏览器对象模型）的一部分，提供了一些方法和属性来操作浏览器窗口和页面。

- Document对象：

  - Document是HTML DOM的一部分，它是HTML页面的根节点，可以访问文档中的所有节点和元素，并且提供了修改文档内容的方法和属性。
  - Document是一个对象，可以通过JavaScript代码进行访问和修改，例如获取元素、添加新元素、修改元素属性等操作。

- Window对象：

  - Window对象是BOM的一部分，代表整个浏览器窗口。除了提供浏览器窗口的尺寸和位置等基本信息外，还提供了一些方法和属性，用于操作浏览器窗口和页面。
  - Window对象是全局对象，可以通过JavaScript代码中的window对象全局访问，并且还有一些属性和方法可以直接调用。
 
#### 总的来说，Document对象和Window对象分别代表了HTML文档和浏览器窗口，它们都是JavaScript中非常重要的对象，用于实现对HTML页面的操作和交互，并提供了丰富的API，方便开发者对HTML页面进行管理和控制。




# 怎么加快首屏加载速度（优化网页的渲染速度）
- 减少HTTP请求：将多个CSS和JavaScript文件合并成一个文件，使用CSS Sprites技术，减少图片的HTTP请求次数。

- 压缩文件大小：使用压缩工具（如Gzip）对HTML、CSS、JavaScript等文件进行压缩，减少文件大小。

- 使用CDN加速：使用CDN（Content Delivery Network）来加速静态资源的传输，从而提高网页的加载速度。

- 使用缓存机制：使用缓存机制来减少数据的重复请求，从而提高网页的加载速度。

- 减少DOM操作：减少DOM操作可以减少浏览器的重排和重绘，从而提高网页的渲染速度。

- 使用异步加载：使用异步加载技术（如defer和async）来延迟JavaScript文件的加载，从而提高网页的加载速度。

- 使用图片懒加载：使用图片懒加载技术来延迟图片的加载，从而提高网页的加载速度。

- 使用CSS动画：使用CSS动画来代替JavaScript动画，从而减少JavaScript的执行时间，提高网页的渲染速度。

- 使用Web字体：使用Web字体可以减少图片的使用，从而提高网页的加载速度。
# js 数据类型以及存放位置

# js 判断数据类型的方法

# js 事件循环机制

## 事件循环机制：

- js 是单线程，为了防止代码阻塞，把任务分为：同步和异步任务
- 同步代码交给 js 引擎执行，异步代码交给宿主环境(node 或者浏览器)
- 同步代码放入执行栈中，异步代码等待特殊时机(比如定时器倒计时完成，点击按钮触发回调函数)送入到任务队列（分为微任务队列和宏任务队列）
- 先执行执行栈中的同步任务，由于微任务比宏任务先执行，就会先去查看微任务队列中是否有微任务，如果有就执行，没有就查看宏任务队列，有就执行，没有就继续查看微任务队列，反复循环，这个过程就是事件循环

# this 的指向
#### JavaScript 中的 this 关键字指向当前函数执行的上下文，它的指向是动态的，根据函数的调用方式而变化。

- 作为普通函数调用，this 指向 window
- 作为对象的方法调用，this 指向这个对象
- 使用 new 关键字对构造函数进行实例化，this 指向实例化的对象
- 箭头函数没有属于⾃⼰的 this，this 的指向由外层作用域决定，与函数的调用方式无关
- 使用 call(),apply(),bind(),this 绑定这些方法的第一个参数
- 严格模式下，this 默认为 undefined
- setTimeout()的回调函数里面的 this 默认 指向 window 对象，所以用箭头函数可以直接获取到上下文的 this，可以不用变量保存 this

# 闭包
#### 闭包是指在函数内部定义的函数，它可以访问外部函数中的变量和参数，并将这些变量和参数的值保存在自己的作用域内。闭包可以将这些变量和参数的值保留下来，使得这些值即使在外部函数执行完毕后仍然可以被内部函数使用。

#### 在JavaScript中，每个函数都会创建一个作用域。当一个函数执行完毕后，它的作用域会被销毁，其中的变量和参数也会被销毁。但是，在一个函数内部定义的函数，因为它们可以访问外部函数的变量和参数，所以它们在执行完毕后仍然可以访问这些变量和参数，这就是闭包的概念。

#### 闭包经常用于实现函数的某些特殊功能，例如在JavaScript中实现私有变量。通过在函数内部定义一个闭包，可以将某些变量和函数的作用域限定在函数内部，从而实现私有变量的效果。

# 原型和原型链
#### 在 JavaScript 中，每个对象都有一个原型（prototype）属性，它指向另一个对象，这个对象就是该对象的原型。原型可以看作是一个模板，包含了可以被该对象实例共享的属性和方法。如果一个对象访问属性或方法时，在该对象本身找不到，就会去它的原型对象中查找，如果还找不到，就会去原型对象的原型对象中查找，以此类推，形成了原型链。
# 作用域和作用域链

# var，let 和 const 的区别

# js 继承

# new 操作符具体干了什么呢？如何实现？

#### 过程：

- 创建一个空对象，作为实例对象。
- 将实例对象的原型指向构造函数的 prototype 属性
- 将构造函数的 this 指向实例对象，执行构造函数的代码（为这个新对象添加属性）
- 判断函数的返回值类型，如果是值类型，返回创建的对象。如果是引用类型，就返回这个引用类型的对象。

#### 实现：

```js
function objectFactory() {
  let newObject = null,
    constructor = Array.prototype.shift.call(arguments),
    result = null;

  // 参数判断
  if (typeof constructor !== "function") {
    console.error("type error");
    return;
  }

  // 新建一个空对象，对象的原型为构造函数的 prototype 对象
  newObject = Object.create(constructor.prototype);

  // 将 this 指向新建对象，并执行函数
  result = constructor.apply(newObject, arguments);

  // 判断返回对象
  let flag =
    result && (typeof result === "object" || typeof result === "function");

  // 判断返回结果
  return flag ? result : newObject;
}

// 使用方法
// objectFactory(构造函数, 初始化参数);
```

# javascript 代码中的 "use strict"; 是什么意思 ? 使用它区别是什么？

#### use strict 是一种 ECMAscript5 添加的（严格）运行模式，这种模式使得 Javascript 在更严格的条件下运行。

#### 设立"严格模式"的目的，主要有以下几个：

- 消除 Javascript 语法的一些不合理、不严谨之处，减少一些怪异行为;
- 消除代码运行的一些不安全之处，保证代码运行的安全；
- 提高编译器效率，增加运行速度；
- 为未来新版本的 Javascript 做好铺垫。

#### 区别：

- 禁止使用 with 语句。
- 禁止 this 关键字指向全局对象。
- 对象不能有重名的属性。

#### 回答：

#### use strict 指的是严格运行模式，在这种模式对 js 的使用添加了一些限制。比如说禁止 this 指向全局对象，还有禁止使用 with 语句等。设立严格模式的目的，主要是为了消除代码使用中的一些不安全的使用方式，也是为了消除 js 语法本身的一些不合理的地方，以此来减少一些运行时的怪异的行为。同时使用严格运行模式也能够提高编译的效率，从而提高代码的运行速度。我认为严格模式代表了 js 一种更合理、更安全、更严谨的发展方向。

# 什么是 Promise 对象，什么是 Promises/A+ 规范？

### Promise 对象是异步编程的一种解决方案，最早由社区提出。Promises/A+ 规范是 JavaScript Promise 的标准，规定了一个 Promise 所必须具有的特性。

### Promise 是一个构造函数，接收一个函数作为参数，返回一个 Promise 实例。一个 Promise 实例有三种状态，分别是 pending、resolved 和 rejected，分别代表了进行中、已成功和已失败。实例的状态只能由 pending 转变 resolved 或者 rejected 状态，并且状态一经改变，就凝固了，无法再被改变了。状态的改变是通过 resolve() 和 reject() 函数来实现的，我们可以在异步操作结束后调用这两个函数改变 Promise 实例的状态，它的原型上定义了一个 then 方法，使用这个 then 方法可以为两个状态的改变注册回调函数。这个回调函数属于微任务，会在本轮事件循环的末尾执行。

# cookie，sessionStorage 和 sessionStorage 的联系和区别
- 作用范围不同：cookie 用于在客户端和服务端之间传递数据；localStorage 和 sessionStorage 用于在客户端持久化存储数据，分别在全部会话和当前会话中有效。

- 存储大小不同：cookie 的大小和数量在不同浏览器中有限制；localStorage 和 sessionStorage 的大小也有限制，在一般情况下为 5MB 左右。

- 数据存储方式不同：cookie 可以被客户端和服务端读取和修改；localStorage 和 sessionStorage 只能在客户端中使用，不会被发送到服务端。

- 生命周期不同：cookie 可以设置过期时间，可以在一定时间内保留数据；localStorage 永久保存数据，除非用户手动删除或者清除浏览器缓存；sessionStorage 只在当前会话中有效，在关闭浏览器或者标签页时会被清除。

# for in 和 for of 的区别

```md
# for... in ...:主要用来遍历对象中可枚举(enumerable 值为 true)的属性，包括原型链上可继承的属性，一般用来遍历对象，如果是数组的话，for...in 循环有几个缺点。

- 数组的键名是数字，但是 for...in 循环是以字符串作为键名“0”、“1”、“2”等等。
- for...in 循环不仅遍历数字键名，还会遍历手动添加的其他键，甚至包括原型链上的键。
- 某些情况下，for...in 循环会以任意顺序遍历键名。

# 所以遍历数组一般用数组自己的方法，map()或者 forEach()
```

```md
# for...of...用来遍历可迭代的数据结构：（不可以遍历对象）

# 可迭代：部署了 Symbol.iterator 属性的数据结构，凡是部署了 Symbol.iterator 属性的数据结构，就称为部署了迭代器接口。调用这个接口，就会返回一个迭代器对象。该对象的根本特征就是具有 next 方法。每次调用 next 方法，都会返回一个代表当前成员的信息对象，具有 value 和 done 两个属性。

原生具备 Iterator 接口的数据结构如下：

- Array
- String
- Map
- Set
- TypedArray（类数组）：函数的 arguments 对象和 NodeList 对象
- Generator 对象
```

# 什么是类数组
#### 类数组是 JavaScript 中一种特殊的对象。它们表现出非常类似数组的特征，但由于它们不适合使用标准 array 方法，因此可以说它们不是真正的数组。类数组具有 “length” 属性，并且可以使用索引来访问各个元素。例如：DOM NodeLists 和 arguments 变量都可以认为是类数组。但是由于它们不使用 Array.prototype上的方法，因此无法使用常见的数组方法，例如 map()、forEach()、push() 等。
#### 使用 Array.from()，Array.prototype.slice.call()将类数组转化为数组

# 遍历对象的方法
ES6 一共有 5 种方法可以遍历对象的属性。
- for...in：for...in循环遍历对象自身的和继承的可枚举属性（不含 Symbol 属性）。
- Object.keys(obj)：返回一个数组，包括对象自身的（不含继承的）所有可枚举属性（不含 Symbol 属性）的键名。
- Object.getOwnPropertyNames(obj)：返回一个数组，包含对象自身的所有 Symbol 属性的键名。
- Object.getOwnPropertySymbols(obj)：返回一个数组，包含对象自身的所有 Symbol 属性的键名。
- Reflect.ownKeys()：返回一个数组，包含对象自身的（不含继承的）所有键名，不管键名是 Symbol 或字符串，也不管是否可枚举。
#### 以上的 5 种方法遍历对象的键名，都遵守同样的属性遍历的次序规则。
- 首先遍历所有数值键，按照数值升序排列。
- 其次遍历所有字符串键，按照加入时间升序排列。
- 最后遍历所有 Symbol 键，按照加入时间升序排列。

```js
Reflect.ownKeys({ [Symbol()]:0, b:0, 10:0, 2:0, a:0 })
// ['2', '10', 'b', 'a', Symbol()]
```
上面代码中，Reflect.ownKeys方法返回一个数组，包含了参数对象的所有属性。这个数组的属性次序是这样的，首先是数值属性2和10，其次是字符串属性b和a，最后是 Symbol 属性。

# 数组的常用方法以及返回值

# 深拷贝与浅拷贝的理解以及怎么实现？

```md
# 浅拷贝：如果属性是基本类型，拷贝的就是基本类型的值，如果属性是引用类型，拷贝的就是内存地址（新旧对象共享同一块内存），所以如果其中一个对象改变了这个地址，就会影响到另一个对象（只是拷贝了指针，使得两个指针指向同一个地址，这样在对象块结束，调用函数析构的时，会造成同一份资源析构 2 次，即 delete 同一块内存 2 次，造成程序崩溃）
```

```md
# 深拷贝： 深拷贝是将一个对象从内存中完整的拷贝一份出来,从堆内存中开辟一个新的区域存放新对象（新旧对象不共享同一块内存）,且修改新对象不会影响原对象（深拷贝采用了在堆内存中申请新的空间来存储数据，这样每个可以避免指针悬挂）
```

## 实现方式：

### 浅拷贝：

#### 数组：

- slice 和 concat 方法
- Array.from()
- 扩展运算符

#### 对象：

- Object.assign
- 扩展运算符

### 深拷贝：

- JSON.parse(JSON.stringify(object)),缺点：会忽略 undefined、symbol 和函数，因为他们不能序列化
- 手写递归实现
- lodash 的-.cloneDeep()方法
- window.structuredClone()方法

#### 数组：

- 浅拷贝指的是将一个对象的属性值复制到另一个对象，如果有的属性的值为引用类型的话，那么会将这个引用的地址复制给对象，因此两个对象会有同一个引用类型的引用。浅拷贝可以使用 Object.assign 和展开运算符来实现。

- 深拷贝相对浅拷贝而言，如果遇到属性值为引用类型的时候，它新建一个引用类型并将对应的值复制给它，因此对象获得的一个新的引用类型而不是一个原有类型的引用。深拷贝对于一些对象可以使用 JSON 的两个函数来实现，但是由于 JSON 的对象格式比 js 的对象格式更加严格，所以如果属性值里边出现函数或者 Symbol 类型的值时，会转换失败。

# 跨域

# js 延迟加载的方式有哪些？

# ES6 新特性

- “class“
- "let 和 const"
- “箭头函数“
- “解构赋值“
- “字符串模板“
- “promise“
- “async/await“（es7）
- “引入 module 模块“
- "Iterator"和 for...of...
- “generators(生成器)“
- “symbol“
- "Map 和 Set"
- "Proxy"和"Reflect"

# 三种事件模型是什么？

#### 事件是用户操作网页时发生的交互动作或者网页本身的一些操作，现代浏览器一共有三种事件模型。

- 第一种事件模型是最早的 DOM0 级模型，这种模型不会传播，所以没有事件流的概念，但是现在有的浏览器支持以冒泡的方式实现，它可以在网页中直接定义监听函数，也可以通过 js 属性来指定监听函数。这种方式是所有浏览器都兼容的。

- 第二种事件模型是 IE 事件模型，在该事件模型中，一次事件共有两个过程，事件处理阶段，和事件冒泡阶段。事件处理阶段会首先执行目标元素绑定的监听事件。然后是事件冒泡阶段，冒泡指的是事件从目标元素冒泡到 document，依次检查经过的节点是否绑定了事件监听函数，如果有则执行。这种模型通过 attachEvent 来添加监听函数，可以添加多个监听函数，会按顺序依次执行。

- 第三种是 DOM2 级事件模型，在该事件模型中，一次事件共有三个过程，第一个过程是事件捕获阶段。捕获指的是事件从 document 一直向下传播到目标元素，依次检查经过的节点是否绑定了事件监听函数，如果有则执行。后面两个阶段和 IE 事件模型的两个阶段相同。这种事件模型，事件绑定的函数是 addEventListener，其中第三个参数可以指定事件是否在捕获阶段执行。

# 事件委托是什么？

#### 事件委托本质上是利用了浏览器事件冒泡的机制。因为事件在冒泡过程中会上传到父节点，并且父节点可以通过事件对象获取到目标节点，因此可以把子节点的监听函数定义在父节点上，由父节点的监听函数统一处理多个子元素的事件，这种方式称为事件代理。

#### 使用事件代理我们可以不必要为每一个子元素都绑定一个监听事件，这样减少了内存上的消耗。并且使用事件代理我们还可以实现事件的动态绑定，比如说新增了一个子节点，我们并不需要单独地为它添加一个监听事件，它所发生的事件会交给父元素中的监听函数来处理。

# Vue2 和 3 的区别
- 更好的性能：Vue.js 3在编译器和运行时方面进行了优化，从而提高了性能。例如，Vue.js 3的编译器使用了更快的静态分析算法，生成的代码更小更快；运行时使用了Proxy代理对象，在数据追踪方面更高效。

- 更好的TypeScript支持：Vue.js 3对TypeScript的支持更加友好，从而提高了代码的可维护性和可读性。例如，Vue.js 3的API和组件选项都使用了泛型类型，可以更好地支持类型检查和自动完成。

- 更好的组合式API：Vue.js 3引入了组合式API，让开发者可以更好地组织和重用逻辑代码。组合式API使用了函数式编程的思想，将相关的逻辑代码组合成可复用的函数，从而提高了代码的可读性和可维护性。

- 更好的响应式系统：Vue.js 3对响应式系统进行了改进，从而提高了性能和可维护性。例如，Vue.js 3使用了Proxy代理对象代替了Vue.js 2中的defineProperty，从而支持更多的数据类型并提高了性能；同时，Vue.js 3还引入了reactive函数和ref函数，从而提高了响应式系统的灵活性和可读性。

- 更好的Tree-shaking支持：Vue.js 3支持更好的Tree-shaking，可以在构建时自动移除没有使用的代码，从而减小构建文件的体积。

- 数据响应式的原理变化：
  - Vue2：使用 Object.defineProperty 对 data 中的数据实现数据劫持(缺点，不能侦测到对象属性的增加与删除，需要另外的 API 以及不能对数组的数据进行数据劫持，需要通过重写数组方法来实现)
  - Vue3：使用 Proxy 与 Reflect 实现数据的响应式，因为 Proxy 可以直接监听对象和数组的变化
- 生命周期的变化：Vue3 中的生命周期相对于 Vue2 做了一些调整，命名上发生了一些变化并且移除了 beforeCreate 和 created，因为 setup 是围绕 beforeCreate 和 created 生命周期钩子运行的，所以不再需要它们。
- v-if 与 v-for 优先级的变化：Vue2 v-for 优先级高，Vue3 v-if 优先级高
# vue2响应式原理：
Vue.js 2.x的响应式原理主要是依靠Object.defineProperty()方法实现的。具体的实现步骤如下：

在Vue实例化时，将data对象中的所有属性遍历到一个Observer对象中，并将每个属性都转换为getter和setter。

在getter中，收集当前属性的所有依赖（即watcher），并把它们加入到一个依赖收集器（Dep）中。

在setter中，如果新值和旧值不相同，则触发依赖收集器中所有依赖的更新函数（即通知所有watcher更新视图）。

在模板编译过程中，如果发现模板中使用了一个data属性，就会创建一个watcher对象，并将该watcher对象加入到该属性对应的依赖收集器中。

当data属性的值发生变化时，setter方法会触发该属性对应的依赖收集器中所有watcher对象的更新函数，从而更新视图。

总之，Vue.js 2.x的响应式原理主要是通过Object.defineProperty()方法实现的，通过getter和setter方法来实现依赖收集和更新视图的功能，从而实现了数据和视图之间的双向绑定。
# MVC 和 MVVM 模式的特点与区别

```md
# MVC:Model 代表数据存储，主要用于实现数据的持久化；View 代表用户界面(UI)，主要用于实现页面的显示；Controller 代表业务逻辑，串联起 View 和 Model，主要用来实现业务的逻辑代码。在 MVC 模式中，用户的交互行为在 View 中触发，由 View 通知 Controller 去进行对应的逻辑处理，处理完成之后通知 Model 改变状态，Model 完成状态改变后，找到对应的 View 去更新用户界面的显示内容，至此完成对用户交互行为的反馈。由此可见，整个流程由 View 发起，最终在 View 中做出改变，这是一个单向的过程。当年流行的 backbone.js 就是 MVC 的典型代表。
```

```md
# MVVM:MVVM 是把 MVC 中的 Controller 去除了，相当于变薄了，取而代之的是 ViewModel。所谓 ViewModel，是一个同步的 View 和 Model 的对象，在前端 MVVM 中，ViewModel 最典型的作用是操作 DOM，特点是双向数据绑定(Data-Binding)。在双向数据绑定中，开发者无须关注如何找到 DOM 节点和如何修改 DOM 节点，因为每一个在 View 中需要操作的 DOM 都会有一个在 Model 中对应的对象，通过改变这个对象，DOM 就会自动改变；反之，当 DOM 改变时，对应的 Model 中的对象也会改变。ViewModel 将 View 和 Model 关联起来，因此开发者只需关注业务逻辑，不需要手动操作 DOM，这就是 ViewModel 带来的优势
```

# Vue 响应式原理

# Vue 组件间通信的方式

- 父传子：props ,子传父：自定义事件 emit
- provide 与 inject
- 事件总线
- vue 的全局状态管理器：Vuex 与 pinia(区别)
- 在父组件使用 ref 获取子组件实例

# Vue diff 算法

#### diff 算法的作用：diff 算法是用来计算两组子节点的差异，并试图最大程度地复用 DOM 元素。

- 最原始的方法更新子节点：卸载所有的旧子节点，再挂载所有的新子节点。这种更新方式无法对 DOM 元素进行复用，需要大量的 DOM 操作才能完成更新，非常消耗性能。于是改进：遍历新旧两组子节点中数量较少的那一组，并逐个调用 patch 函数进行打补丁，然后比较新旧两组子节点的数量，如果新的一组的子节点数更多，说明有新子节点需要挂载；否则就说明在旧的一组子节点中，有节点需要卸载。
- key 的作用：key 值就像是虚拟节点的“身份证号”，只要两个虚拟节点的 type 值和 key 值都相同，那么就可以进行 DOM 节点的复用（可以复用不一定不需要更新，仍需要对两个虚拟节点进行打补丁操作）。在没有 key 的情况下，Vue 将使用一种最小化元素移动的算法，并尽可能地就地更新/复用相同类型的元素。如果传了 key，则将根据 key 的变化顺序来重新排列元素，并且将始终移除/销毁 key 已经不存在的元素。所以我们就需要知道如何寻找需要移动的节点

- 简单 diff 算法：
  - 找到可复用的 DOM 进行更新：只要两个虚拟节点的 type 值和 key 值都相同，那么就可以进行 DOM 节点的复用（可以复用不一定不需要更新，仍需要对两个虚拟节点进行打补丁操作），两层 for 循环，外层循环遍历新的一组子节点，内层循环遍历旧的一组子节点。在内层循环中，逐个对比新旧子节点的 key 值，如果在旧子节点中找到可复用的节点，则调用 patch 函数进行打补丁。这样就可以保证所有可复用的节点本身都已经更新完毕了。
  - 找到需要移动的元素：(最大索引：在旧子节点中寻找具有相同 key 值节点的过程中，遇到的最大索引值)，拿新的一组子节点中的节点去旧的一组子节点中寻找可复用的节点。如果找到了，则记录该节点的位置索引，把这个位置索引称为最大索引。在整个更新过程中，如果一个节点的索引值小于最大索引(不需要更新的情况是最大索引值递增)，则说明该节点对应的真实 DOM 元素需要移动(移动之前需要用 patch 函数进行打补丁)
  - 如何移动节点：移动节点是指：移动一个虚拟节点所对应的真是 DOM 节点，并不是移动虚拟节点本身，所以得获得真实 DOM 节点的引用，即 vnode.el 属性。在更新操作时，渲染器会调用 patchElement 函数在新旧虚拟节点之间打补丁，在函数内部有一个赋值语句：const el = n2.el = n1.el(nl:旧虚拟节点，n2:新虚拟节点)，所以复用了 DOM 元素之后，新节点也持有了对真实 DOM 的引用。所以在整个更新过程中，当找到的索引值小于最大索引值的时候，获取当前新子节点的前一个节点，如果该前驱节点不存在，说明该新子节点是第一个节点，不需要移动，否则，获取该前驱节点对应真实 DOM 的下一个兄弟节点，将其作为锚点，然后用 insert 方法将该新子节点对应的真实 DOM 插入到锚点元素前面，也就是前驱节点对应真实节点的后面，insert 方法内部依赖了浏览器原生的 insertBefore 方法
  - 如何新增节点：首先，在外层循环定义一个 find 变量，代表渲染器是否能在旧的一组子节点中找到可复用的节点。变量 find 的初始值为 false，一道寻找到可复用的节点，则将变量 find 的值设置为 true。如果内层循环结束后，变量 find 的值仍为 false，则说明当前的新虚拟节点是一个全新的节点，需要挂载它。为了将节点挂载到正确位置，我们需要先获取锚点元素，找到当前新虚拟节点的前驱节点，如果存在，则使用它对应的真实 DOM 的下一个兄弟节点作为锚点元素；如果不存在，则说明将挂载的新虚拟节点是容器元素的第一个子节点，此时应该使用容器元素的 container.firstChild 作为锚点元素。最后，将锚点元素 anchor 作为 patch 函数的第四个参数，调用 patch 函数完成节点的挂载
  - 移除不存在的元素：当基本更新完成之后，再遍历旧的一组子节点，然后去新的一组子节点中寻找具有相同 key 值的节点。如果找不到，说明应该删除该节点，用 unmount 函数将其卸载
- 双端 diff 算法：
  - 同时对新旧两组子节点的两个端点进行比较，获取新旧两端子节点的索引值，再获取对应的节点，然后依次比较旧头新头，旧尾新尾，旧头新尾和旧尾新头节点的 key 值是否向相同；
    - 理想情况：如果相同，则先用 patch 函数进行更新，然后再进行 DOM 元素的移动，最后在对当前索引值进行更新，向各自正确的方向前进一步，并指向下一个节点，循环的终止条件时任意一个头节点的索引值大于对应尾节点的索引值；
    - 非理想情况：如果经过比较之后，都没有可以复用的节点，需要增加额外的处理步骤来处理：拿新的一组子节点中的头部节点去旧的一组子节点中寻找是否有 key 值相同的节点。假设在旧子节点组中索引为 1 的位置上找到了可以复用的节点，意味着这个节点在新节点中并不是头部节点，但是在更新之后，变成了头部节点，所以需要将该节点对应的真实 DOM 移动到当前旧的一组子节点的头部节点所对应的真实 DOM 节点之前(移动操作之前还需打补丁)，由于该索引值对应的真实 DOM 已经移动到别处，将其设置为 undefined，然后再更新新头部节点的索引值继续比较，所以我们可以再循环的逻辑再加一层，旧子节点的头部和尾部节点是否存在，如果不存在则证明它们已经被处理过了，直接跳下一个位置即可。
    - 添加新元素：当我们在第一轮比较中没有找到可复用的节点，然后拿新的一组子节点中的头部节点去旧的一组子节点中寻找，也没找到可复用的节点，所以我们要在循环结束后检查索引值的情况，当旧尾索引值小于旧头索引值，且新头索引值小于等于新尾索引值，就说明有新的节点遗漏，需要挂载它们，于是增加一个 for 循环来挂载索引值位于新头和新尾之间的新节点。挂载时的锚点仍然使用当前的头部节点 oldStartVNode.el
    - 移除不存在的元素，与处理新节点类似，在 while 循环结束后加入一个 else if 的分支，当新尾索引值小于新头索引值，且旧头索引值小于等于旧尾索引值，，需要增加一个 for 循环来卸载索引值位于旧头和旧尾之间的旧节点。
  - 优势：减少 DOM 移动操作的次数

# vue 中 key 值的作用？

#### key 值就像是虚拟节点的“身份证号”，只要两个虚拟节点的 type 值和 key 值都相同，那么就可以进行 DOM 节点的复用（可以复用不一定不需要更新，仍需要对两个虚拟节点进行打补丁操作）。在没有 key 的情况下，Vue 将使用一种最小化元素移动的算法，并尽可能地就地更新/复用相同类型的元素。如果传了 key，则将根据 key 的变化顺序来重新排列元素，并且将始终移除/销毁 key 已经不存在的元素。

# v-if和v-show的区别
- `v-if` 是“真实的”按条件渲染，因为它确保了在切换时，条件区块内的事件监听器和子组件都会被销毁与重建。`v-if` 也是惰性的：如果在初次渲染时条件值为 `false`，则不会做任何事。条件区块只有当条件首次变为 `true` 时才被渲染。

- 相比之下，`v-show` 简单许多，元素无论初始条件如何，始终会被渲染，只有 CSS `display` 属性会被切换。

#### 总的来说，`v-if` 有更高的切换开销，而 `v-show` 有更高的初始渲染开销。因此，如果需要频繁切换，则使用 `v-show` 较好；如果在运行时绑定条件很少改变，则 `v-if` 会更合适。
# computed 和 watch 的差异？

- computed 是计算一个新的属性，并将该属性挂载到 Vue 实例上，而 watch 是监听已经存在且已挂载到 Vue 实例上的数据，所以用 watch 同样可以监听 computed 计算属性的变化。

- computed 本质是一个惰性求值的观察者，具有缓存性，只有当依赖变化后，第一次访问 computed 属性，才会计算新的值。而 watch 则是当数据发生变化便会调用执行函数。

- 从使用场景上说，computed 适用一个数据被多个数据影响，而 watch 适用一个数据影响多个数据。

# 观察者和发布订阅模式的区别

### 发布订阅模式实际上是广义上的观察者模式：发布订阅模式是最常用的一种观察者模式的实现，并且从解耦和重用角度来看，更优于典型的观察者模式

#### 在观察者模式中，观察者需要直接订阅目标事件。在目标发出内容改变的事件之后，直接接收事件并作出响应

#### 在发布订阅模式中，发布者和订阅者之间多了一个调度中心。调度中心一方面从发布者接收事件，另一方面向订阅者发布事件，订阅者需要在调度中心中订阅事件。通过调度中心实现了发布者和订阅者之间关系的解耦。使用发布订阅模式更利于我们代码的可维护性。

# Vue 的生命周期

## Vue2：

- beforeCreate 在实例初始化之后，数据观测(data observer) 和 event/watcher 事件配置之前被调用。在当前阶段 data、methods、computed 以及 watch 上的数据和方法都不能被访问
- created 实例已经创建完成之后被调用。在这一步，实例已完成以下的配置：数据观测(data observer)，属性和方法的运算， watch/event 事件回调。这里没有$el,如果非要想与 Dom 进行交互，可以通过 vm.$nextTick 来访问 Dom
- beforeMount 在挂载开始之前被调用：相关的 render 函数首次被调用。
- mounted 在挂载完成后发生，在当前阶段，真实的 Dom 挂载完毕，数据完成双向绑定，可以访问到 Dom 节点
- beforeUpdate 数据更新时调用，发生在虚拟 DOM 重新渲染和打补丁（patch）之前。可以在这个钩子中进一步地更改状态，这不会触发附加的重渲染过程
- updated 发生在更新完成之后，当前阶段组件 Dom 已完成更新。要注意的是避免在此期间更改数据，因为这可能会导致无限循环的更新，该钩子在服务器端渲染期间不被调用。
- beforeDestroy 实例销毁之前调用。在这一步，实例仍然完全可用。我们可以在这时进行善后收尾工作，比如清除计时器。
- destroyed Vue 实例销毁后调用。调用后，Vue 实例指示的所有东西都会解绑定，所有的事件监听器会被移除，所有的子实例也会被销毁。 该钩子在服务器端渲染期间不被调用。
- activated keep-alive 专属，组件被激活时调用
- deactivated keep-alive 专属，组件被销毁时调用

```md
# 常见面试题：异步请求在哪一步发起？

# 可以在钩子函数 created、beforeMount、mounted 中进行异步请求，因为在这三个钩子函数中，data 已经创建，可以将服务端端返回的数据进行赋值。
```

```md
# vue 可不可以在 created 钩子操作 dom

# 使用 nextTick,将 dom 操作放在回调函数里
```

# vue 路由跳转的原理

```md
# hash 模式：地址栏带#符号，每次哈希值变化都会调用 hashChange 事件。优点：兼容性好，刷新不会重新加载页面。缺点：不美观

# history 模式：利用的是 HTML5 新增的 pushState()和 replaceState()方法，push 会留下历史记录，replace 不会留下历史记录。优点：美观；缺点：兼容性，刷新会 404，需要后端配置，例如 Nginx 配置 try_files，
```

# v-model 的原理

```md
# 文本类型的 <input> 和 <textarea> 元素会绑定 value property 并侦听 input 事件；

# <input type="checkbox"> 和 <input type="radio"> 会绑定 checked property 并侦听 change 事件；

# <select> 会绑定 value property 并侦听 change 事件。
```

# H5 新特性

- 语义化标签
- 音视频标签
- input 标签的 type 值（email,tel,search）
- input 新增表单属性(required,placeholder,autofocus,autocomplete,multiple)

# 简述一下你对 HTML 语义化的理解？

#### html 语义化主要指的是开发者应该使用合适的标签来划分网页内容的结构。html 的本质作用其实就是定义网页文档的结构，一个语义化的文档，能够使页面的结构更加清晰，易于理解。这样不仅有利于开发者的维护和理解，同时也能够使机器对文档内容进行正确的解读。比如说我们常用的 b 标签和 strong 标签，它们在样式上都是文字的加粗，但是 strong 标签拥有强调的语义。对于一般显示来说，可能我们看上去没有差异，但是对于机器来说，就会有很大的不同。如果用户使用的是屏幕阅读器来访问网页的话，使用 strong 标签就会有明显的语调上的变化，而 b 标签则没有。如果是搜索引擎的爬虫对我们网页进行分析的话，那么它会依赖于 html 标签来确定上下文和各个关键字的权重，一个语义化的文档对爬虫来说是友好的，是有利于爬虫对文档内容解读的，从而有利于我们网站的 SEO。从 html5 我们可以看出，标准是倾向于以语义化的方式来构建网页的，比如新增了 header 、footer 这些语义标签，删除了 big，font 这些没有语义的标签。

# C3 新特性

- 属性选择器 div[type = xxx]
- 结构伪类选择器 E:first-child,last-child,nth-child(n)
- 伪元素选择器

# CSS 中常用的单位

- em：有继承性，在 font-size 中使用是相对于父元素的字体大小，在其他属性中使用是相对于自身的字体大小，如 width，height，padding
- rem：根元素的字体大小
- vw：视窗宽度的 1%
- vh：视窗高度的 1%

# BFC

```md
块格式化上下文（Block Formatting Context，BFC）是 Web 页面的可视化 CSS 渲染的一部分，是布局过程中生成块级盒子的区域，也是浮动元素与其他元素的交互限定区域。
```

#### 通俗来讲

- BFC 是一个独立的布局环境，可以理解为一个容器，在这个容器中按照一定规则进行物品摆放，并且不会影响其它环境中的物品。
- 如果一个元素符合触发 BFC 的条件，则 BFC 中的元素布局不受外部影响。

#### 解决什么问题：

- 解决浮动元素使父元素高度塌陷
- 外边距重叠（为其中一个元素的外边包裹一层父元素，并且触发父元素 BFC）
- 浮动元素重叠（解决自适应布局的问题）：PC 端的网页，左右两栏布局很常见，一般左侧定宽，右侧主体页面宽度自适应变化，通常是用浮动来实现的；它利用了块级元素占满一行的特性，使得右边的元素可以随着页面宽度的变化而变化，又利用了浮动的特性，让左侧元素覆盖在右侧元素上方，同时还能挤开下方元素的内容，让页面看起来是两栏的效果，但随着右边元素的增加，超出了左边元素的高度后，文字就会环绕左侧元素，这显然不是我们想要的效果，因为右侧元素触发了 BFC，触发 BFC 的容器就是页面上的一个完全隔离开的容器，容器中的子元素绝对不会影响到外面的元素，为了保证这个规则，触发了 BFC 的右侧元素为了将内部元素和左侧浮动元素隔离开，不得不形成这样左右完全隔离的两栏，同时，如果右侧元素依旧是块级元素，那么他尽可能占满一行的特性还在，这样就保证了右侧元素依旧是自适应的

#### 怎么触发 BFC：

- 根元素（html），或者包含 body 的元素
- overflow 的值为非 visible（hidden，auto，scroll）
- display 的值为:inline-block,flow-root（无副作用但是不兼容 IE）,grid,flex,table,table-cell
- position 的值为:fixed 或者 absolute
- float 的值不为 none（left 或者 right）

# link 和 @import 的区别

- link 是 HTML 标签，不仅可以加载 CSS 文件，还可以定义 RSS、rel 连接属性等；@import 是 CSS 提供的语法，只有导入样式表的作用。
- 加载页面时，link 标签引入的 CSS 被同时加载；@import 引入的 CSS 将在页面加载完毕后被加载。
- @import 是 CSS2.1 才有的语法，故只可在 IE5+ 才能识别；link 标签作为 HTML 元素，不存在兼容性问题。
- 可以通过 JS 操作 DOM ，插入 link 标签来改变样式；由于 DOM 方法是基于文档的，无法使用@import 的方式插入样式。
- link 引入的样式权重大于@import 引入的样式。

# position 属性

- static 默认值。没有定位，元素出现在正常的流中（忽略 top,bottom,left,right,z-index 声明）

- relative 生成相对定位的元素，不影响元素本身特性， 不会使元素脱离文档流， 没有定位偏移量时对元素无影响（相对于自身原本位置进行偏移），提升层级（用 z-index 样式的值可以改变一个定位元素的层级关系，从而改变元素的覆盖关系，值越大越在上面，z-index 只能在 position 属性值为 relative 或 absolute 或 fixed 的元素上有效。） （两个都为定位元素，后面的会覆盖前面的定位）

- absolute 生成绝对定位的元素， 使元素完全脱离文档流（在文档流中不再占位），使内联元素在设置宽高的时候支持宽高，使区块元素在未设置宽度时由内容撑开宽度，相对于最近一个有定位的父元素偏移（若其父元素没有定位则逐层上找，直到 document——页面文档对象），相对定位一般配合绝对定位使用，提升层级
- fixed（老 IE 不支持）生成绝对定位的元素，相对于浏览器窗口进行定位

- sticky 粘性定位可以被认为是相对定位和固定定位的混合。元素在跨越特定阈值前为相对定位，之后为固定定位。须指定 top, right, bottom 或 left 四个阈值其中之一，才可使粘性定位生效。否则其行为与相对定位相同。

# 如何垂直和水平居中

```md
一般常见的几种居中的方法有：

对于宽高固定的元素

（1）我们可以利用 margin:0 auto 来实现元素的水平居中。

（2）利用绝对定位，设置四个方向的值都为 0，并将 margin 设置为 auto，由于宽高固定，因此对应方向实现平分，可以实现水
平和垂直方向上的居中。

（3）利用绝对定位，先将元素的左上角通过 top:50%和 left:50%定位到页面的中心，然后再通过 margin 负值来调整元素
的中心点到页面的中心。

（4）利用绝对定位，先将元素的左上角通过 top:50%和 left:50%定位到页面的中心，然后再通过 translate 来调整元素
的中心点到页面的中心。

（5）使用 flex 布局，通过 align-items:center 和 justify-content:center 设置容器的垂直和水平方向上为居中对
齐，然后它的子元素也可以实现垂直和水平的居中。

对于宽高不定的元素，上面的后面两种方法，可以实现元素的垂直和水平的居中。
```

# CSS 选择器

- id 选择器（#myid）
- 类选择器（.myclassname）
- 标签选择器（div,h1,p）
- 后代选择器（h1 p）
- 相邻后代选择器（子）选择器（ul>li）
- 兄弟选择器（li~a）
- 相邻兄弟选择器（li+a）
- 属性选择器（a[rel="external"]）
- 伪类选择器（a:hover,li:nth-child）
- 伪元素选择器（::before、::after）
- 通配符选择器（\*）

# 画一个三角形

#### 采用的是相邻边框连接处的均分原理。

```css
将元素的宽高设为0，只设置border，把任意三条边隐藏掉（颜色设为transparent），剩下的就是一个三角形。
  #demo {
  width: 0;
  height: 0;
  border-width: 20px;
  border-style: solid;
  border-color: transparent transparent red transparent;
}
```
# CSS Modules是什么
CSS Modules 是一种 CSS 方案，用于在模块化的 JavaScript 应用程序中管理样式。它通过在编译时为每个类名生成唯一的哈希字符串来实现样式的封装，从而使每个模块的样式独立于其他模块。

使用 CSS Modules 可以解决样式命名冲突的问题，并且可以通过在 JavaScript 中直接引用类名来实现样式的复用。

例如，假设您有一个名为 button.css 的样式文件，其中包含以下样式：
```css
.button {
  background-color: blue;
  color: white;
  font-size: 16px;
  padding: 10px 20px;
  border-radius: 4px;
}

```
使用 CSS Modules，您可以在 JavaScript 文件中通过以下方式引用这些样式：
```js
import styles from './button.css';

const button = document.createElement('button');
button.className = styles.button;
```
在这种情况下，.button 类名将会被编译成一个唯一的哈希字符串，并自动添加到 styles 对象的 button 属性上。这样，您就可以通过引用 `styles.button` 来使用这些样式，而不必担心命名冲突的问题。

使用 CSS Modules 还有一个好处是，它可以让您在编写样式时更方便地使用 JavaScript 变量。例如，您可以在样式文件中使用 :export 关键字来导出 JavaScript 变量，并在 JavaScript 中通过 import 语句引用这些变量。
```css
:export {
  primaryColor: blue;
  secondaryColor: green;
}

.button {
  color: primaryColor;
}

```
在 JavaScript 文件中，您可以通过以下方式引用这些样式：
```js
import { primaryColor, secondaryColor } from './colors.css';

const button = document.createElement('button');
button.style.color = primaryColor;
```
CSS Modules 可以通过使用 Webpack 或其他构建工具来实现，并且可以与 React、Vue.js 等框架很好地配合使用。它是一种很好的解决方案，可以让您在模块化的应用程序中更好地管理样式。
# DOMContentLoaded 事件和 Load 事件的区别？

- 当初始的 HTML 文档被完全加载和解析完成之后，DOMContentLoaded 事件被触发，而无需等待样式表、图像和子框架的加载完成。

- Load 事件是当所有资源加载完成后触发的。

# xss 和 csrf 是什么，如何防范

```md
# XSS 攻击指的是跨站脚本攻击，是一种代码注入攻击。攻击者通过在网站注入恶意脚本，使之在用户的浏览器上运行，从而盗取用户的信息如 cookie 等。

## XSS 的本质是因为网站没有对恶意代码进行过滤，与正常的代码混合在一起了，浏览器没有办法分辨哪些脚本是可信的，从而导致了恶意代码的执行。

#### XSS 一般分为存储型、反射型和 DOM 型。

- 存储型指的是恶意代码提交到了网站的数据库中，当用户请求数据的时候，服务器将其拼接为 HTML 后返回给了用户，从而导致了恶意代码的执行。

- 反射型指的是攻击者构建了特殊的 URL，当服务器接收到请求后，从 URL 中获取数据，拼接到 HTML 后返回，从而导致了恶意代码的执行。

- DOM 型指的是攻击者构建了特殊的 URL，用户打开网站后，js 脚本从 URL 中获取数据，从而导致了恶意代码的执行。

## XSS 攻击的预防可以从两个方面入手，一个是恶意代码提交的时候，一个是浏览器执行恶意代码的时候。

- 对于第一个方面，如果我们对存入数据库的数据都进行的转义处理，但是一个数据可能在多个地方使用，有的地方可能不需要转义，由于我们没有办法判断数据最后的使用场景，所以直接在输入端进行恶意代码的处理，其实是不太可靠的.因此我们可以从浏览器的执行来进行预防，一种是使用纯前端的方式，不用服务器端拼接后返回。另一种是对需要插入到 HTML 中的代码做好充分的转义。对于 DOM 型的攻击，主要是前端脚本的不可靠而造成的，我们对于数据获取渲染和字符串拼接的时候应该对可能出现的恶意代码情况进行判断。

- 还有一些方式，比如使用 CSP ，CSP 的本质是建立一个白名单，告诉浏览器哪些外部资源可以加载和执行，从而防止恶意代码的注入攻击。

- 还可以对一些敏感信息进行保护，比如 cookie 使用 http-only ，使得脚本无法获取。也可以使用验证码，避免脚本伪装成用户执行一些操作。
```

```md
# CSRF 攻击指的是跨站请求伪造攻击，攻击者诱导用户进入一个第三方网站，然后该网站向被攻击网站发送跨站请求。如果用户在被攻击网站中保存了登录状态，那么攻击者就可以利用这个登录状态，绕过后台的用户验证，冒充用户向服务器执行一些操作。

## CSRF 攻击的本质是利用了 cookie 会在同源请求中携带发送给服务器的特点，以此来实现用户的冒充。

#### 一般的 CSRF 攻击类型有三种：

- 第一种是 GET 类型的 CSRF 攻击，比如在网站中的一个 img 标签里构建一个请求，当用户打开这个网站的时候就会自动发起提
  交。

- 第二种是 POST 类型的 CSRF 攻击，比如说构建一个表单，然后隐藏它，当用户进入页面时，自动提交这个表单。

- 第三种是链接类型的 CSRF 攻击，比如说在 a 标签的 href 属性里构建一个请求，然后诱导用户去点击。

#### CSRF 可以用下面几种方法来防护：

- 第一种是同源检测的方法，服务器根据 http 请求头中 origin 或者 referer 信息来判断请求是否为允许访问的站点，从而对请求进行过滤。当 origin 或者 referer 信息都不存在的时候，直接阻止。这种方式的缺点是有些情况下 referer 可以被伪造。还有就是我们这种方法同时把搜索引擎的链接也给屏蔽了，所以一般网站会允许搜索引擎的页面请求，但是相应的页面请求这种请求方式也可能被攻击者给利用。

- 第二种方法是使用 CSRF Token 来进行验证，服务器向用户返回一个随机数 Token ，当网站再次发起请求时，在请求参数中加入服务器端返回的 token ，然后服务器对这个 token 进行验证。这种方法解决了使用 cookie 单一验证方式时，可能会被冒用的问题，但是这种方法存在一个缺点就是，我们需要给网站中的所有请求都添加上这个 token，操作比较繁琐。还有一个问题是一般不会只有一台网站服务器，如果我们的请求经过负载平衡转移到了其他的服务器，但是这个服务器的 session 中没有保留这个 token 的话，就没有办法验证了。这种情况我们可以通过改变 token 的构建方式来解决。

- 第三种方式使用双重 Cookie 验证的办法，服务器在用户访问网站页面时，向请求域名注入一个 Cookie，内容为随机字符串，然后当用户再次向服务器发送请求的时候，从 cookie 中取出这个字符串，添加到 URL 参数中，然后服务器通过对 cookie 中的数据和参数中的数据进行比较，来进行验证。使用这种方式是利用了攻击者只能利用 cookie，但是不能访问获取 cookie 的特点。并且这种方法比 CSRF Token 的方法更加方便，并且不涉及到分布式访问的问题。这种方法的缺点是如果网站存在 XSS 漏洞的，那么这种方式会失效。同时这种方式不能做到子域名的隔离。

- 第四种方式是使用在设置 cookie 属性的时候设置 Samesite ，限制 cookie 不能作为被第三方使用，从而可以避免被攻击者利用。Samesite 一共有两种模式，一种是严格模式，在严格模式下 cookie 在任何情况下都不可能作为第三方 Cookie 使用，在宽松模式下，cookie 可以被请求是 GET 请求，且会发生页面跳转的请求所使用。
```
## 跟跨网站脚本（XSS）相比，XSS 利用的是用户对指定网站的信任，CSRF 利用的是网站对用户网页浏览器的信任。

# 开发中常用的几种 Content-Type ？

- application/x-www-form-urlencoded

浏览器的原生 form 表单，如果不设置 enctype 属性，那么最终就会以 application/x-www-form-urlencoded 方式提交数据。该种方式提交的数据放在 body 里面，数据按照 key1=val1&key2=val2 的方式进行编码，key 和 val 都进行了 URL
转码。

- multipart/form-data

该种方式也是一个常见的 POST 提交方式，通常表单上传文件时使用该种方式。

- application/json

告诉服务器消息主体是序列化后的 JSON 字符串。

- text/xml

该种方式主要用来提交 XML 格式的数据。

# eval 是做什么的？

#### 它的功能是把对应的字符串解析成 JS 代码并运行。

#### 应该避免使用 eval，不安全，非常耗性能（2 次，一次解析成 js 语句，一次执行）。

# 浏览器的渲染原理

- HTML解析：浏览器首先会将HTML代码解析成DOM树。在解析过程中，浏览器会根据HTML标签和属性的含义，将其转换成对应的DOM节点和属性。

- CSS解析：浏览器会将CSS样式表解析成CSS对象模型（CSS Object Model，简称CSSOM）。在解析过程中，浏览器会将CSS样式转换成浏览器可以理解的格式，并将其应用到DOM节点上。

- 布局（Layout）：布局是指浏览器根据DOM节点和CSS样式计算出每个节点在屏幕上的位置和大小。布局过程中，浏览器会遍历DOM树，根据节点的类型和样式计算出每个节点的位置和大小。

- 绘制（Painting）：绘制是指浏览器将布局计算出来的节点绘制到屏幕上。绘制过程中，浏览器会将节点转换成像素，并将其绘制到屏幕上。

- 合成（Compositing）：合成是指浏览器将绘制出来的图层合成到屏幕上。合成过程中，浏览器会将所有图层合并成一个整体，并将其显示在屏幕上。


# 事件委托：

```md
# 事件委托是利用事件流的特征解决一些开发需求的知识技巧

# 事件委托本质上是利用了浏览器事件冒泡的机制。因为事件在冒泡过程中会上传到父节点，并且父节点可以通过事件对象获取到目标节点，因此可以把子节点的监听函数定义在父节点上，由父节点的监听函数统一处理多个子元素的事件，这种方式称为事件代理。

# 使用事件代理我们可以不必要为每一个子元素都绑定一个监听事件，这样减少了内存上的消耗。并且使用事件代理我们还可以实现事件的动态绑定，比如说新增了一个子节点，我们并不需要单独地为它添加一个监听事件，它所发生的事件会交给父元素中的监听函数来处理。
```

# DNS 完整的查询过程:

- 首先会在「浏览器的缓存」中查找对应的 IP 地址，如果查找到直接返回，若找不到继续下一步
- 将请求发送给「本地 DNS 服务器」，在本地 DNS 服务器缓存中查询，如果查找到，就直接将查找结果返回，若找不到继续下一步
- 本地 DNS 服务器向「根域名服务器」发送请求，根域名服务器会返回一个所查询域的顶级域名服务器地址
- 本地 DNS 服务器向「顶级域名服务器」发送请求，接受请求的服务器查询自己的缓存，如果有记录，就返回查询结果，如果没有就返回相关的下一级的权威域名服务器的地址
- 本地 DNS 服务器向「权威域名服务器」发送请求，域名服务器返回对应的结果
- 本地 DNS 服务器将返回结果保存在缓存中，便于下次使用
- 本地 DNS 服务器将返回结果返回给浏览器

### 递归查询和迭代查询

```md
# 递归查询:指的是查询请求发出后，域名服务器代为向下一级域名服务器发出请求，最后向用户返回查询的最终结果。使用递归查询，用户只需要发出一次查询请求。

# 迭代查询指的是查询请求后，域名服务器返回单次查询的结果。下一级的查询由用户自己请求。使用迭代查询，用户需要发出 多次的查询请求。
```

```md
# 一般我们向本地 DNS 服务器发送请求的方式就是递归查询，因为我们只需要发出一次请求，然后本地 DNS 服务器返回给我 们最终的请求结果。而本地 DNS 服务器向其他域名服务器请求的过程是迭代查询的过程，因为每一次域名服务器只返回单次 查询的结果，下一级的查询由本地 DNS 服务器自己进行。
```

# 代码输出题

```js
setTimeout(() => {
  console.log("setTimeout start"); //5
  new Promise((resolve) => {
    console.log("promise1 start"); //6
    resolve();
  }).then(() => {
    console.log("promise1 end"); //8
  });
  console.log("setTimeout end"); //7
}, 0);
function promise2() {
  return new Promise((resolve) => {
    console.log("promise2"); //2
    resolve();
  });
}
async function async1() {
  console.log("async1 start"); //1
  await promise2();
  console.log("async1 end"); //4
}
async1();
console.log("script end"); //3
//函数不调用不执行，async是同步，new Promise是同步，await下一行的代码是异步微任务
```
