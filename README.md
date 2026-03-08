<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>你的名字 - 个人主页</title>
    <!-- 引入Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- 引入图标库 -->
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    
    <!-- 自定义配置 -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#6366f1', // 主色调（紫色系）
                        secondary: '#10b981', // 辅助色（绿色系）
                        dark: '#1e293b',
                        light: '#f8fafc'
                    },
                    fontFamily: {
                        sans: ['Inter', 'system-ui', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    
    <style type="text/tailwindcss">
        @layer utilities {
            .text-gradient {
                background-clip: text;
                -webkit-background-clip: text;
                -webkit-text-fill-color: transparent;
            }
            .bg-gradient-custom {
                background: linear-gradient(135deg, #6366f1 0%, #10b981 100%);
            }
            .card-hover {
                transition: all 0.3s ease;
            }
            .card-hover:hover {
                transform: translateY(-5px);
                box-shadow: 0 10px 25px -5px rgba(99, 102, 241, 0.1), 0 8px 10px -6px rgba(99, 102, 241, 0.1);
            }
        }
    </style>
</head>

<body class="bg-light dark:bg-dark text-gray-800 dark:text-gray-200 min-h-screen transition-colors duration-300">
    <!-- 导航栏 -->
    <nav class="fixed w-full bg-white/80 dark:bg-dark/80 backdrop-blur-sm z-50 shadow-sm">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <a href="#home" class="text-xl font-bold text-gradient bg-gradient-custom">你的名字</a>
            
            <!-- 桌面导航 -->
            <div class="hidden md:flex space-x-8">
                <a href="#home" class="hover:text-primary transition-colors">首页</a>
                <a href="#about" class="hover:text-primary transition-colors">关于我</a>
                <a href="#skills" class="hover:text-primary transition-colors">技能</a>
                <a href="#projects" class="hover:text-primary transition-colors">项目</a>
                <a href="#contact" class="hover:text-primary transition-colors">联系我</a>
            </div>
            
            <!-- 暗黑模式切换 -->
            <button id="theme-toggle" class="p-2 rounded-full hover:bg-gray-100 dark:hover:bg-gray-800 transition-colors">
                <i class="fa fa-moon-o dark:hidden" aria-hidden="true"></i>
                <i class="fa fa-sun-o hidden dark:inline" aria-hidden="true"></i>
            </button>
            
            <!-- 移动端菜单按钮 -->
            <button id="menu-toggle" class="md:hidden p-2">
                <i class="fa fa-bars" aria-hidden="true"></i>
            </button>
        </div>
        
        <!-- 移动端导航菜单 -->
        <div id="mobile-menu" class="md:hidden hidden bg-white dark:bg-dark shadow-lg">
            <div class="container mx-auto px-4 py-2 flex flex-col space-y-3">
                <a href="#home" class="py-2 hover:text-primary transition-colors">首页</a>
                <a href="#about" class="py-2 hover:text-primary transition-colors">关于我</a>
                <a href="#skills" class="py-2 hover:text-primary transition-colors">技能</a>
                <a href="#projects" class="py-2 hover:text-primary transition-colors">项目</a>
                <a href="#contact" class="py-2 hover:text-primary transition-colors">联系我</a>
            </div>
        </div>
    </nav>

    <!-- 首页 Hero 区域 -->
    <section id="home" class="pt-32 pb-20 px-4 bg-gradient-custom/5 dark:bg-gradient-custom/10">
        <div class="container mx-auto max-w-4xl">
            <div class="flex flex-col md:flex-row items-center gap-8">
                <div class="w-full md:w-1/2">
                    <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-4">
                        你好，我是 <span class="text-gradient bg-gradient-custom">你的名字</span>
                    </h1>
                    <p class="text-xl mb-8 text-gray-600 dark:text-gray-400">
                        一名充满热情的【你的职业，如：前端开发者/全栈工程师/UI设计师】
                    </p>
                    <div class="flex flex-wrap gap-4">
                        <a href="#projects" class="px-6 py-3 bg-primary text-white rounded-full hover:bg-primary/90 transition-colors">
                            查看我的项目
                        </a>
                        <a href="#contact" class="px-6 py-3 border border-primary text-primary rounded-full hover:bg-primary/10 transition-colors">
                            联系我
                        </a>
                    </div>
                </div>
                <div class="w-full md:w-1/2 flex justify-center">
                    <!-- 头像区域 -->
                    <div class="relative w-64 h-64 rounded-full overflow-hidden border-4 border-white dark:border-gray-800 shadow-xl">
                        <!-- 替换为你的头像URL -->
                        <img src="https://picsum.photos/400/400" alt="个人头像" class="w-full h-full object-cover">
                        <div class="absolute inset-0 bg-gradient-custom/20"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 关于我 -->
    <section id="about" class="py-20 px-4">
        <div class="container mx-auto max-w-4xl">
            <h2 class="text-3xl font-bold mb-12 text-center">关于我</h2>
            <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-md p-8 card-hover">
                <p class="text-lg leading-relaxed mb-6">
                    嗨！我是【你的名字】，一名专注于【你的领域，如：Web开发/移动端开发/设计】的工程师/设计师。
                    拥有【X年】的工作/学习经验，热爱技术，喜欢探索新的技术栈和解决方案。
                </p>
                <p class="text-lg leading-relaxed mb-6">
                    除了编程/设计，我还喜欢【你的爱好，如：阅读、旅行、摄影、健身】，
                    相信持续学习和跨界思考能带来更多的创意和灵感。
                </p>
                <p class="text-lg leading-relaxed">
                    我始终坚持写出优雅、可维护、高性能的代码/设计出用户体验优秀的产品，
                    期待能和更多优秀的人一起合作，创造有价值的产品。
                </p>
            </div>
        </div>
    </section>

    <!-- 技能展示 -->
    <section id="skills" class="py-20 px-4 bg-gray-50 dark:bg-gray-900">
        <div class="container mx-auto max-w-4xl">
            <h2 class="text-3xl font-bold mb-12 text-center">我的技能</h2>
            <div class="grid grid-cols-2 md:grid-cols-3 gap-6">
                <!-- 技能卡片 1 -->
                <div class="bg-white dark:bg-gray-800 rounded-xl p-6 text-center card-hover">
                    <i class="fa fa-code text-4xl text-primary mb-4" aria-hidden="true"></i>
                    <h3 class="text-xl font-semibold mb-2">前端开发</h3>
                    <p class="text-gray-600 dark:text-gray-400">HTML/CSS/JavaScript、React、Vue、TailwindCSS</p>
                </div>
                <!-- 技能卡片 2 -->
                <div class="bg-white dark:bg-gray-800 rounded-xl p-6 text-center card-hover">
                    <i class="fa fa-server text-4xl text-primary mb-4" aria-hidden="true"></i>
                    <h3 class="text-xl font-semibold mb-2">后端开发</h3>
                    <p class="text-gray-600 dark:text-gray-400">Node.js、Python、Java、MySQL、MongoDB</p>
                </div>
                <!-- 技能卡片 3 -->
                <div class="bg-white dark:bg-gray-800 rounded-xl p-6 text-center card-hover">
                    <i class="fa fa-paint-brush text-4xl text-primary mb-4" aria-hidden="true"></i>
                    <h3 class="text-xl font-semibold mb-2">设计能力</h3>
                    <p class="text-gray-600 dark:text-gray-400">Figma、Photoshop、UI/UX设计、原型设计</p>
                </div>
                <!-- 技能卡片 4 -->
                <div class="bg-white dark:bg-gray-800 rounded-xl p-6 text-center card-hover">
                    <i class="fa fa-github text-4xl text-primary mb-4" aria-hidden="true"></i>
                    <h3 class="text-xl font-semibold mb-2">版本控制</h3>
                    <p class="text-gray-600 dark:text-gray-400">Git、GitHub、GitLab、CI/CD</p>
                </div>
                <!-- 技能卡片 5 -->
                <div class="bg-white dark:bg-gray-800 rounded-xl p-6 text-center card-hover">
                    <i class="fa fa-cloud text-4xl text-primary mb-4" aria-hidden="true"></i>
                    <h3 class="text-xl font-semibold mb-2">云服务</h3>
                    <p class="text-gray-600 dark:text-gray-400">AWS、阿里云、腾讯云、Docker</p>
                </div>
                <!-- 技能卡片 6 -->
                <div class="bg-white dark:bg-gray-800 rounded-xl p-6 text-center card-hover">
                    <i class="fa fa-language text-4xl text-primary mb-4" aria-hidden="true"></i>
                    <h3 class="text-xl font-semibold mb-2">语言能力</h3>
                    <p class="text-gray-600 dark:text-gray-400">中文（母语）、英语（CET-6）、日语（N3）</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 项目展示 -->
    <section id="projects" class="py-20 px-4">
        <div class="container mx-auto max-w-4xl">
            <h2 class="text-3xl font-bold mb-12 text-center">我的项目</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <!-- 项目卡片 1 -->
                <div class="bg-white dark:bg-gray-800 rounded-xl overflow-hidden shadow-md card-hover">
                    <img src="https://picsum.photos/600/400?random=1" alt="项目截图" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-2">项目名称 1</h3>
                        <p class="text-gray-600 dark:text-gray-400 mb-4">
                            项目简短描述：这是一个基于React开发的电商网站，实现了商品展示、购物车、支付等核心功能。
                        </p>
                        <div class="flex gap-4">
                            <a href="https://github.com/你的用户名/项目名" target="_blank" class="text-primary hover:underline">
                                <i class="fa fa-github mr-1" aria-hidden="true"></i> 源码
                            </a>
                            <a href="https://你的演示地址.com" target="_blank" class="text-primary hover:underline">
                                <i class="fa fa-external-link mr-1" aria-hidden="true"></i> 演示
                            </a>
                        </div>
                    </div>
                </div>
                <!-- 项目卡片 2 -->
                <div class="bg-white dark:bg-gray-800 rounded-xl overflow-hidden shadow-md card-hover">
                    <img src="https://picsum.photos/600/400?random=2" alt="项目截图" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-2">项目名称 2</h3>
                        <p class="text-gray-600 dark:text-gray-400 mb-4">
                            项目简短描述：这是一个基于Python的数据分析工具，能够快速处理和可视化大规模数据集。
                        </p>
                        <div class="flex gap-4">
                            <a href="https://github.com/你的用户名/项目名" target="_blank" class="text-primary hover:underline">
                                <i class="fa fa-github mr-1" aria-hidden="true"></i> 源码
                            </a>
                            <a href="https://你的演示地址.com" target="_blank" class="text-primary hover:underline">
                                <i class="fa fa-external-link mr-1" aria-hidden="true"></i> 演示
                            </a>
                        </div>
                    </div>
                </div>
                <!-- 项目卡片 3 -->
                <div class="bg-white dark:bg-gray-800 rounded-xl overflow-hidden shadow-md card-hover">
                    <img src="https://picsum.photos/600/400?random=3" alt="项目截图" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-2">项目名称 3</h3>
                        <p class="text-gray-600 dark:text-gray-400 mb-4">
                            项目简短描述：这是一个移动端小程序，提供了便捷的日常任务管理和提醒功能。
                        </p>
                        <div class="flex gap-4">
                            <a href="https://github.com/你的用户名/项目名" target="_blank" class="text-primary hover:underline">
                                <i class="fa fa-github mr-1" aria-hidden="true"></i> 源码
                            </a>
                            <a href="https://你的演示地址.com" target="_blank" class="text-primary hover:underline">
                                <i class="fa fa-external-link mr-1" aria-hidden="true"></i> 演示
                            </a>
                        </div>
                    </div>
                </div>
                <!-- 项目卡片 4 -->
                <div class="bg-white dark:bg-gray-800 rounded-xl overflow-hidden shadow-md card-hover">
                    <img src="https://picsum.photos/600/400?random=4" alt="项目截图" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-2">项目名称 4</h3>
                        <p class="text-gray-600 dark:text-gray-400 mb-4">
                            项目简短描述：这是一个开源的UI组件库，包含了50+常用组件，支持主题定制。
                        </p>
                        <div class="flex gap-4">
                            <a href="https://github.com/你的用户名/项目名" target="_blank" class="text-primary hover:underline">
                                <i class="fa fa-github mr-1" aria-hidden="true"></i> 源码
                            </a>
                            <a href="https://你的演示地址.com" target="_blank" class="text-primary hover:underline">
                                <i class="fa fa-external-link mr-1" aria-hidden="true"></i> 演示
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 联系方式 -->
    <section id="contact" class="py-20 px-4 bg-gray-50 dark:bg-gray-900">
        <div class="container mx-auto max-w-4xl">
            <h2 class="text-3xl font-bold mb-12 text-center">联系我</h2>
            <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-md p-8 max-w-2xl mx-auto card-hover">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                    <div>
                        <h3 class="text-xl font-semibold mb-4">联系方式</h3>
                        <ul class="space-y-4">
                            <li class="flex items-center">
                                <i class="fa fa-envelope text-primary text-xl mr-4" aria-hidden="true"></i>
                                <span>your-email@example.com</span>
                            </li>
                            <li class="flex items-center">
                                <i class="fa fa-github text-primary text-xl mr-4" aria-hidden="true"></i>
                                <a href="https://github.com/你的用户名" target="_blank" class="hover:text-primary transition-colors">github.com/你的用户名</a>
                            </li>
                            <li class="flex items-center">
                                <i class="fa fa-linkedin text-primary text-xl mr-4" aria-hidden="true"></i>
                                <a href="https://linkedin.com/in/你的用户名" target="_blank" class="hover:text-primary transition-colors">linkedin.com/in/你的用户名</a>
                            </li>
                            <li class="flex items-center">
                                <i class="fa fa-weixin text-primary text-xl mr-4" aria-hidden="true"></i>
                                <span>你的微信号</span>
                            </li>
                        </ul>
                    </div>
                    <div>
                        <h3 class="text-xl font-semibold mb-4">发送消息</h3>
                        <form class="space-y-4">
                            <div>
                                <label for="name" class="block mb-2 text-sm">姓名</label>
                                <input type="text" id="name" class="w-full px-4 py-2 border border-gray-300 dark:border-gray-700 rounded-lg bg-white dark:bg-gray-800 focus:outline-none focus:ring-2 focus:ring-primary">
                            </div>
                            <div>
                                <label for="email" class="block mb-2 text-sm">邮箱</label>
                                <input type="email" id="email" class="w-full px-4 py-2 border border-gray-300 dark:border-gray-700 rounded-lg bg-white dark:bg-gray-800 focus:outline-none focus:ring-2 focus:ring-primary">
                            </div>
                            <div>
                                <label for="message" class="block mb-2 text-sm">消息</label>
                                <textarea id="message" rows="3" class="w-full px-4 py-2 border border-gray-300 dark:border-gray-700 rounded-lg bg-white dark:bg-gray-800 focus:outline-none focus:ring-2 focus:ring-primary"></textarea>
                            </div>
                            <button type="submit" class="px-6 py-2 bg-primary text-white rounded-lg hover:bg-primary/90 transition-colors">
                                发送消息
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer class="bg-dark text-white py-8 px-4">
        <div class="container mx-auto max-w-4xl text-center">
            <p class="mb-4">© 2025 你的名字 - 个人主页</p>
            <div class="flex justify-center space-x-6">
                <a href="https://github.com/你的用户名" target="_blank" class="hover:text-primary transition-colors">
                    <i class="fa fa-github text-xl" aria-hidden="true"></i>
                </a>
                <a href="https://twitter.com/你的用户名" target="_blank" class="hover:text-primary transition-colors">
                    <i class="fa fa-twitter text-xl" aria-hidden="true"></i>
                </a>
                <a href="https://linkedin.com/in/你的用户名" target="_blank" class="hover:text-primary transition-colors">
                    <i class="fa fa-linkedin text-xl" aria-hidden="true"></i>
                </a>
                <a href="https://zhihu.com/people/你的用户名" target="_blank" class="hover:text-primary transition-colors">
                    <i class="fa fa-globe text-xl" aria-hidden="true"></i>
                </a>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        // 移动端菜单切换
        const menuToggle = document.getElementById('menu-toggle');
        const mobileMenu = document.getElementById('mobile-menu');
        
        menuToggle.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });
        
        // 暗黑模式切换
        const themeToggle = document.getElementById('theme-toggle');
        const html = document.documentElement;
        
        // 初始化主题
        if (localStorage.theme === 'dark' || (!('theme' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
            html.classList.add('dark');
        } else {
            html.classList.remove('dark');
        }
        
        // 切换主题
        themeToggle.addEventListener('click', () => {
            html.classList.toggle('dark');
            if (html.classList.contains('dark')) {
                localStorage.theme = 'dark';
            } else {
                localStorage.theme = 'light';
            }
        });
        
        // 平滑滚动
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                // 关闭移动端菜单
                mobileMenu.classList.add('hidden');
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // 导航栏滚动效果
        window.addEventListener('scroll', () => {
            const nav = document.querySelector('nav');
            if (window.scrollY > 50) {
                nav.classList.add('shadow-md');
                nav.classList.remove('shadow-sm');
            } else {
                nav.classList.remove('shadow-md');
                nav.classList.add('shadow-sm');
            }
        });
        
        // 表单提交处理
        document.querySelector('form').addEventListener('submit', (e) => {
            e.preventDefault();
            alert('消息发送成功！我会尽快回复你。');
            e.target.reset();
        });
    </script>
</body>
</html>
