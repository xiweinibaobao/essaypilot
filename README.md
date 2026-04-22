<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>EssayPilot - 留学生申请文书写作系统</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            cream: '#FCFBF8',
            sage: '#7A8B70',
            sageDark: '#6A7A60',
            lavender: '#E1DDF7',
            lavenderDark: '#D1CDE8',
            textDark: '#2C3327'
          }
        }
      }
    }
  </script>
</head>
<body class="min-h-screen bg-cream text-textDark font-sans">

  <header class="sticky top-0 z-20 border-b border-stone-200 bg-cream/90 backdrop-blur">
    <div class="mx-auto flex max-w-7xl items-center justify-between px-6 py-4">
      <div>
        <div class="text-xl font-semibold tracking-tight text-textDark">EssayPilot</div>
        <div class="text-sm text-stone-500">留学生申请文书写作系统</div>
      </div>
      <nav class="hidden gap-2 md:flex" id="nav-menu">
        <button onclick="navigate('home')" data-target="home" class="nav-btn rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer bg-sage text-white hover:bg-sageDark">首页</button>
        <button onclick="navigate('dashboard')" data-target="dashboard" class="nav-btn rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer text-stone-600 hover:bg-stone-100">工作台</button>
        <button onclick="navigate('builder')" data-target="builder" class="nav-btn rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer text-stone-600 hover:bg-stone-100">文书工坊</button>
        <button onclick="navigate('schools')" data-target="schools" class="nav-btn rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer text-stone-600 hover:bg-stone-100">院校版本</button>
        <button onclick="navigate('pricing')" data-target="pricing" class="nav-btn rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer text-stone-600 hover:bg-stone-100">定价</button>
      </nav>
      <div class="flex gap-3">
        <button class="rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer border border-stone-200 text-stone-700 hover:bg-stone-50">登录</button>
        <button class="rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer bg-sage text-white hover:bg-sageDark">免费开始</button>
      </div>
    </div>
  </header>

  <main id="main-content">
    <div id="page-home" class="page-section">
      <section class="mx-auto grid max-w-7xl gap-10 px-6 py-16 md:grid-cols-2 md:py-24">
        <div class="flex flex-col justify-center">
          <div class="w-fit"><span class="inline-flex rounded-full px-3 py-1 text-xs font-medium bg-lavender text-[#3B3554]">英美硕士申请 · PS / SOP 优先</span></div>
          <h1 class="mt-5 max-w-3xl text-4xl font-semibold tracking-tight text-textDark md:text-6xl">
            把留学申请文书，从“不会写”变成“有流程地写好”
          </h1>
          <p class="mt-5 max-w-2xl text-base leading-7 text-stone-600 md:text-lg">
            不是通用 AI 写作工具，而是一套为申请文书设计的工作流系统：挖素材、定故事线、逐段写作、院校定制、逻辑诊断，再到最终导出和交付。
          </p>
          <div class="mt-8 flex flex-wrap gap-3">
            <button onclick="navigate('dashboard')" class="rounded-2xl px-5 py-3 text-sm font-medium transition-colors cursor-pointer bg-sage text-white hover:bg-sageDark">查看演示工作台</button>
            <button onclick="navigate('pricing')" class="rounded-2xl px-5 py-3 text-sm font-medium transition-colors cursor-pointer border border-stone-200 bg-white hover:bg-stone-50">查看定价</button>
          </div>
          <div class="mt-8 grid max-w-xl grid-cols-3 gap-4 text-sm">
            <div class="rounded-3xl bg-white shadow-sm ring-1 ring-stone-200 p-4">
              <div class="text-2xl font-semibold text-textDark">4 步</div>
              <div class="mt-1 text-stone-500">核心写作流程</div>
            </div>
            <div class="rounded-3xl bg-white shadow-sm ring-1 ring-stone-200 p-4">
              <div class="text-2xl font-semibold text-textDark">多版本</div>
              <div class="mt-1 text-stone-500">院校项目定制</div>
            </div>
            <div class="rounded-3xl bg-white shadow-sm ring-1 ring-stone-200 p-4">
              <div class="text-2xl font-semibold text-textDark">可协作</div>
              <div class="mt-1 text-stone-500">后续接顾问 review</div>
            </div>
          </div>
        </div>

        <div class="rounded-3xl bg-white shadow-sm ring-1 ring-stone-200 p-5">
          <div class="flex items-start justify-between gap-4">
            <div>
              <div class="text-sm font-medium text-stone-500">实时写作面板</div>
              <div class="mt-1 text-lg font-semibold text-textDark">Personal Statement Builder</div>
            </div>
            <span class="inline-flex rounded-full px-3 py-1 text-xs font-medium bg-sage text-white">Live Demo</span>
          </div>

          <div class="mt-5 grid gap-4 md:grid-cols-2">
            <div class="rounded-2xl bg-[#F6F5F2] p-4">
              <div class="text-sm font-medium text-stone-700">当前故事线</div>
              <div class="mt-2 text-xl font-semibold text-textDark">职业目标型</div>
              <p class="mt-2 text-sm leading-6 text-stone-600">从数据分析实习切入，连接课程项目、科研兴趣和毕业后的产品分析职业目标。</p>
            </div>
            <div class="rounded-2xl bg-[#F6F5F2] p-4">
              <div class="text-sm font-medium text-stone-700">文书健康度</div>
              <div class="mt-2 text-xl font-semibold text-textDark">84 / 100</div>
              <p class="mt-2 text-sm leading-6 text-stone-600">结构完整，但第二段证据还不够具体，why program 可继续贴近课程特色。</p>
            </div>
          </div>

          <div class="mt-4 rounded-2xl border border-stone-200 p-4">
            <div class="flex items-center justify-between">
              <div class="text-sm font-medium text-stone-700">生成中的文书大纲</div>
              <div class="text-xs text-stone-500">v1.8</div>
            </div>
            <div class="mt-3 space-y-3 text-sm">
              <div class="rounded-xl bg-[#F6F5F2] p-3">
                <div class="font-medium text-textDark">引子</div>
                <div class="mt-1 text-stone-600">用一次真实数据项目经历引出对数据科学的长期兴趣。</div>
              </div>
              <div class="rounded-xl bg-[#F6F5F2] p-3">
                <div class="font-medium text-textDark">主体段 1</div>
                <div class="mt-1 text-stone-600">课程与科研如何建立技术基础。</div>
              </div>
              <div class="rounded-xl bg-[#F6F5F2] p-3">
                <div class="font-medium text-textDark">主体段 2</div>
                <div class="mt-1 text-stone-600">实习如何帮助确认行业方向与问题意识。</div>
              </div>
              <div class="rounded-xl bg-[#F6F5F2] p-3">
                <div class="font-medium text-textDark">结尾</div>
                <div class="mt-1 text-stone-600">连接目标项目与中长期职业路径。</div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>

    <div id="page-dashboard" class="page-section hidden">
      <section class="mx-auto max-w-7xl px-6 py-12">
        <div class="mb-8 flex flex-col gap-4 md:flex-row md:items-end md:justify-between">
          <div>
            <div class="text-sm font-medium text-stone-500">2027 Fall Application</div>
            <h2 class="mt-1 text-3xl font-semibold tracking-tight text-textDark">学生工作台</h2>
            <p class="mt-2 text-stone-600">查看当前申请进度、项目状态和文书下一步动作。</p>
          </div>
          <button class="rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer bg-sage text-white hover:bg-sageDark">新建申请项目</button>
        </div>

        <div class="grid gap-4 md:grid-cols-4">
          <div class="rounded-3xl bg-white shadow-sm ring-1 ring-stone-200 p-5 md:col-span-2">
            <div class="text-sm font-medium text-stone-500">整体完成度</div>
            <div class="mt-2 text-4xl font-semibold text-textDark">60%</div>
            <div class="mt-4">
              <div class="h-2 rounded-full bg-stone-200"><div class="h-2 rounded-full bg-sage transition-all duration-500 ease-out" style="width: 60%"></div></div>
            </div>
            <div class="mt-3 text-sm text-stone-600">当前共有 3 个目标项目，主文书已完成初稿并进入定制阶段。</div>
          </div>
          <div class="rounded-3xl bg-white shadow-sm ring-1 ring-stone-200 p-5">
            <div class="text-sm font-medium text-stone-500">已提炼素材</div>
            <div class="mt-2 text-4xl font-semibold text-textDark">14</div>
            <div class="mt-3 text-sm text-stone-600">来自课程、科研、实习与竞赛的有效写作素材。</div>
          </div>
          <div class="rounded-3xl bg-white shadow-sm ring-1 ring-stone-200 p-5">
            <div class="text-sm font-medium text-stone-500">待处理问题</div>
            <div class="mt-2 text-4xl font-semibold text-textDark">3</div>
            <div class="mt-3 text-sm text-stone-600">包括证据不足、项目匹配度表达不够清晰等问题。</div>
          </div>
        </div>

        <div class="mt-6 grid gap-6 lg:grid-cols-[1.3fr_0.9fr]">
          <div class="rounded-3xl bg-white shadow-sm ring-1 ring-stone-200 p-5">
            <div class="flex items-center justify-between">
              <div class="text-lg font-semibold text-textDark">申请项目</div>
              <span class="inline-flex rounded-full px-3 py-1 text-xs font-medium bg-lavender text-[#3B3554]">按截止日期排序</span>
            </div>
            <div class="mt-4 space-y-4">
              <div class="rounded-2xl bg-[#F6F5F2] p-4">
                <div class="flex flex-col gap-3 md:flex-row md:items-center md:justify-between">
                  <div>
                    <div class="font-medium text-textDark">UCL MSc Data Science</div>
                    <div class="mt-1 text-sm text-stone-500">UK · Customizing · Deadline 2026-11-20</div>
                  </div>
                  <div class="min-w-28 text-sm font-medium text-textDark">78%</div>
                </div>
                <div class="mt-3"><div class="h-2 rounded-full bg-stone-200"><div class="h-2 rounded-full bg-sage" style="width: 78%"></div></div></div>
              </div>
              <div class="rounded-2xl bg-[#F6F5F2] p-4">
                <div class="flex flex-col gap-3 md:flex-row md:items-center md:justify-between">
                  <div>
                    <div class="font-medium text-textDark">CMU MS Information Systems</div>
                    <div class="mt-1 text-sm text-stone-500">US · Drafting · Deadline 2026-12-15</div>
                  </div>
                  <div class="min-w-28 text-sm font-medium text-textDark">61%</div>
                </div>
                <div class="mt-3"><div class="h-2 rounded-full bg-stone-200"><div class="h-2 rounded-full bg-sage" style="width: 61%"></div></div></div>
              </div>
              <div class="rounded-2xl bg-[#F6F5F2] p-4">
                <div class="flex flex-col gap-3 md:flex-row md:items-center md:justify-between">
                  <div>
                    <div class="font-medium text-textDark">LSE MSc Management</div>
                    <div class="mt-1 text-sm text-stone-500">UK · Outline Ready · Deadline 2026-12-01</div>
                  </div>
                  <div class="min-w-28 text-sm font-medium text-textDark">42%</div>
                </div>
                <div class="mt-3"><div class="h-2 rounded-full bg-stone-200"><div class="h-2 rounded-full bg-sage" style="width: 42%"></div></div></div>
              </div>
            </div>
          </div>

          <div class="rounded-3xl bg-white shadow-sm ring-1 ring-stone-200 p-5">
            <div class="text-lg font-semibold text-textDark">本周进展</div>
            <div class="mt-4 space-y-3">
              <div class="flex gap-3 rounded-2xl bg-[#F6F5F2] p-3">
                <div class="flex h-7 w-7 shrink-0 items-center justify-center rounded-full bg-sage text-xs font-medium text-white">1</div>
                <div><div class="font-medium text-textDark">背景问卷完成</div><div class="mt-1 text-sm text-stone-600">系统已提炼 14 条有效素材</div></div>
              </div>
              <div class="flex gap-3 rounded-2xl bg-[#F6F5F2] p-3">
                <div class="flex h-7 w-7 shrink-0 items-center justify-center rounded-full bg-sage text-xs font-medium text-white">2</div>
                <div><div class="font-medium text-textDark">主故事线确认</div><div class="mt-1 text-sm text-stone-600">职业目标型 + 数据分析实习主线</div></div>
              </div>
              <div class="flex gap-3 rounded-2xl bg-[#F6F5F2] p-3">
                <div class="flex h-7 w-7 shrink-0 items-center justify-center rounded-full bg-sage text-xs font-medium text-white">3</div>
                <div><div class="font-medium text-textDark">PS 大纲生成</div><div class="mt-1 text-sm text-stone-600">引子 / 3 个主体段 / 职业目标结尾</div></div>
              </div>
              <div class="flex gap-3 rounded-2xl bg-[#F6F5F2] p-3">
                <div class="flex h-7 w-7 shrink-0 items-center justify-center rounded-full bg-sage text-xs font-medium text-white">4</div>
                <div><div class="font-medium text-textDark">院校定制中</div><div class="mt-1 text-sm text-stone-600">已完成 UCL 版，CMU 版待补项目 fit</div></div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>

    <div id="page-builder" class="page-section hidden">
      <section class="mx-auto max-w-7xl px-6 py-12">
        <div class="mb-8">
          <div class="text-sm font-medium text-stone-500">Document Studio</div>
          <h2 class="mt-1 text-3xl font-semibold tracking-tight text-textDark">文书工坊</h2>
          <p class="mt-2 text-stone-600">从素材、故事线到逐段改写，控制整篇文书的结构与质量。</p>
        </div>

        <div class="grid gap-6 lg:grid-cols-[0.8fr_1.4fr_0.8fr]">
          <main class="order-first lg:order-none">
            <div class="rounded-3xl bg-white shadow-sm ring-1 ring-stone-200 p-5 h-full">
              <div class="flex items-center justify-between">
                <div>
                  <div class="text-lg font-semibold text-textDark">PS Draft Editor</div>
                  <div class="mt-1 text-sm text-stone-500">UCL 版本 · v2.3</div>
                </div>
                <span class="inline-flex rounded-full px-3 py-1 text-xs font-medium bg-sage text-white">Auto Saved</span>
              </div>
              <div class="mt-5 rounded-2xl border border-stone-200 p-4">
                <div class="text-sm font-medium text-stone-500">当前段落</div>
                <textarea class="mt-3 min-h-[360px] w-full resize-none rounded-2xl bg-[#F6F5F2] p-4 text-sm leading-7 text-stone-700 outline-none focus:ring-2 focus:ring-[#7A8B70]/30 transition-shadow">During my internship in data analytics, I began to see that effective decision-making depends not only on intuition, but on the ability to transform messy user behavior into actionable insights. That experience pushed me to rethink the way I wanted to contribute to digital products. Rather than staying at the level of observation, I wanted to build a stronger technical foundation in statistical reasoning, machine learning, and data-driven problem solving...</textarea>
                <div class="mt-4 flex flex-wrap gap-3">
                  <button class="rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer bg-sage text-white hover:bg-sageDark">继续改写这一段</button>
                  <button class="rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer border border-stone-200 text-stone-700 hover:bg-stone-50">让语气更自然</button>
                  <button class="rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer border border-stone-200 text-stone-700 hover:bg-stone-50">加强项目匹配度</button>
                </div>
              </div>
            </div>
          </main>

          <aside>
            <div class="rounded-3xl bg-white shadow-sm ring-1 ring-stone-200 p-5">
              <div class="text-lg font-semibold text-textDark">素材面板</div>
              <div class="mt-4 space-y-3 text-sm">
                <div class="rounded-2xl bg-[#F6F5F2] p-3 leading-6 text-stone-700">GPA 3.82 / 4.0，统计学与编程课程表现突出</div>
                <div class="rounded-2xl bg-[#F6F5F2] p-3 leading-6 text-stone-700">在互联网公司做数据分析实习，参与用户增长项目</div>
                <div class="rounded-2xl bg-[#F6F5F2] p-3 leading-6 text-stone-700">完成一个推荐系统课程项目并写过研究报告</div>
                <div class="rounded-2xl bg-[#F6F5F2] p-3 leading-6 text-stone-700">职业目标：做数据驱动的产品分析 / 决策支持</div>
              </div>
              <button class="mt-4 w-full rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer border border-stone-200 text-stone-700 hover:bg-stone-50">编辑背景问卷</button>
            </div>
          </aside>

          <aside>
            <div class="rounded-3xl bg-white shadow-sm ring-1 ring-stone-200 p-5">
              <div class="text-lg font-semibold text-textDark">诊断结果</div>
              <div class="mt-4 space-y-3 text-sm">
                <div class="rounded-2xl bg-[#F6F5F2] p-3">
                  <div class="font-medium text-textDark">结构</div>
                  <div class="mt-1 leading-6 text-stone-600">引子清晰，第二段和第三段之间的衔接还可增强</div>
                </div>
                <div class="rounded-2xl bg-[#F6F5F2] p-3">
                  <div class="font-medium text-textDark">证据</div>
                  <div class="mt-1 leading-6 text-stone-600">实习例子具体，但科研经历的细节仍偏少</div>
                </div>
                <div class="rounded-2xl bg-[#F6F5F2] p-3">
                  <div class="font-medium text-textDark">风格</div>
                  <div class="mt-1 leading-6 text-stone-600">整体自然，个别句子略显抽象</div>
                </div>
                <div class="rounded-2xl bg-[#F6F5F2] p-3">
                  <div class="font-medium text-textDark">匹配度</div>
                  <div class="mt-1 leading-6 text-stone-600">why UCL 可以进一步结合课程和研究环境</div>
                </div>
              </div>
              <button class="mt-4 w-full rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer border border-stone-200 text-stone-700 hover:bg-stone-50">重新诊断全文</button>
            </div>
          </aside>
        </div>
      </section>
    </div>

    <div id="page-schools" class="page-section hidden">
      <section class="mx-auto max-w-7xl px-6 py-12">
        <div class="mb-8">
          <div class="text-sm font-medium text-stone-500">School Versions</div>
          <h2 class="mt-1 text-3xl font-semibold tracking-tight text-textDark">院校版本管理</h2>
          <p class="mt-2 text-stone-600">同一份素材，生成适配不同学校与项目的定制文书版本。</p>
        </div>

        <div class="grid gap-4 lg:grid-cols-3">
          <div class="rounded-3xl bg-white shadow-sm ring-1 ring-stone-200 p-5">
            <div class="flex items-start justify-between gap-4">
              <div>
                <div class="text-lg font-semibold text-textDark">UCL</div>
                <div class="mt-1 text-sm text-stone-500">MSc Data Science</div>
              </div>
              <span class="inline-flex rounded-full px-3 py-1 text-xs font-medium bg-lavender text-[#3B3554]">v2.3</span>
            </div>
            <div class="mt-4 text-sm text-stone-600">强调跨学科课程与伦敦数据生态</div>
            <div class="mt-4">
              <div class="mb-2 flex items-center justify-between text-sm">
                <span class="text-stone-600">当前匹配度</span>
                <span class="font-medium text-textDark">88%</span>
              </div>
              <div class="h-2 rounded-full bg-stone-200"><div class="h-2 rounded-full bg-sage" style="width: 88%"></div></div>
            </div>
            <div class="mt-4 flex gap-3">
              <button class="rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer bg-sage text-white hover:bg-sageDark">查看版本</button>
              <button class="rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer border border-stone-200 text-stone-700 hover:bg-stone-50">重新生成</button>
            </div>
          </div>
          <div class="rounded-3xl bg-white shadow-sm ring-1 ring-stone-200 p-5">
            <div class="flex items-start justify-between gap-4">
              <div>
                <div class="text-lg font-semibold text-textDark">CMU</div>
                <div class="mt-1 text-sm text-stone-500">MS Information Systems</div>
              </div>
              <span class="inline-flex rounded-full px-3 py-1 text-xs font-medium bg-lavender text-[#3B3554]">v1.6</span>
            </div>
            <div class="mt-4 text-sm text-stone-600">强调产品化思维与技术管理路径</div>
            <div class="mt-4">
              <div class="mb-2 flex items-center justify-between text-sm">
                <span class="text-stone-600">当前匹配度</span>
                <span class="font-medium text-textDark">81%</span>
              </div>
              <div class="h-2 rounded-full bg-stone-200"><div class="h-2 rounded-full bg-sage" style="width: 81%"></div></div>
            </div>
            <div class="mt-4 flex gap-3">
              <button class="rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer bg-sage text-white hover:bg-sageDark">查看版本</button>
              <button class="rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer border border-stone-200 text-stone-700 hover:bg-stone-50">重新生成</button>
            </div>
          </div>
          <div class="rounded-3xl bg-white shadow-sm ring-1 ring-stone-200 p-5">
            <div class="flex items-start justify-between gap-4">
              <div>
                <div class="text-lg font-semibold text-textDark">LSE</div>
                <div class="mt-1 text-sm text-stone-500">MSc Management</div>
              </div>
              <span class="inline-flex rounded-full px-3 py-1 text-xs font-medium bg-lavender text-[#3B3554]">v1.2</span>
            </div>
            <div class="mt-4 text-sm text-stone-600">强调商业分析与国际化职业目标</div>
            <div class="mt-4">
              <div class="mb-2 flex items-center justify-between text-sm">
                <span class="text-stone-600">当前匹配度</span>
                <span class="font-medium text-textDark">74%</span>
              </div>
              <div class="h-2 rounded-full bg-stone-200"><div class="h-2 rounded-full bg-sage" style="width: 74%"></div></div>
            </div>
            <div class="mt-4 flex gap-3">
              <button class="rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer bg-sage text-white hover:bg-sageDark">查看版本</button>
              <button class="rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer border border-stone-200 text-stone-700 hover:bg-stone-50">重新生成</button>
            </div>
          </div>
        </div>
      </section>
    </div>

    <div id="page-pricing" class="page-section hidden">
      <section class="mx-auto max-w-7xl px-6 py-12">
        <div class="mb-8 text-center">
          <div class="text-sm font-medium text-stone-500">Pricing</div>
          <h2 class="mt-1 text-3xl font-semibold tracking-tight text-textDark">先验证需求，再做精细化定价</h2>
          <p class="mt-2 text-stone-600">这一版先给你一个适合留学文书产品的价格结构参考。</p>
        </div>
        <div class="grid gap-4 lg:grid-cols-3">
          <div class="rounded-3xl bg-white shadow-sm ring-1 ring-stone-200 p-6">
            <div class="flex items-start justify-between gap-3">
              <div><div class="text-xl font-semibold text-textDark">Starter</div><div class="mt-2 text-3xl font-semibold text-textDark">¥79</div></div>
            </div>
            <div class="mt-3 text-sm leading-6 text-stone-600">适合先生成第一版 PS / SOP 的学生</div>
            <div class="mt-5 space-y-3 text-sm text-stone-700">
              <div class="rounded-2xl bg-[#F6F5F2] px-3 py-2">1 个申请项目</div>
              <div class="rounded-2xl bg-[#F6F5F2] px-3 py-2">PS / SOP 初稿</div>
              <div class="rounded-2xl bg-[#F6F5F2] px-3 py-2">基础结构诊断</div>
              <div class="rounded-2xl bg-[#F6F5F2] px-3 py-2">导出 PDF</div>
            </div>
            <button class="mt-6 w-full py-3 rounded-2xl px-4 text-sm font-medium transition-colors cursor-pointer border border-stone-200 text-stone-700 hover:bg-stone-50">选择 Starter</button>
          </div>
          <div class="rounded-3xl bg-white shadow-sm ring-2 ring-sage p-6">
            <div class="flex items-start justify-between gap-3">
              <div><div class="text-xl font-semibold text-textDark">Standard</div><div class="mt-2 text-3xl font-semibold text-textDark">¥199</div></div>
              <span class="inline-flex rounded-full px-3 py-1 text-xs font-medium bg-sage text-white">推荐</span>
            </div>
            <div class="mt-3 text-sm leading-6 text-stone-600">适合正式申请季使用</div>
            <div class="mt-5 space-y-3 text-sm text-stone-700">
              <div class="rounded-2xl bg-[#F6F5F2] px-3 py-2">5 个院校版本</div>
              <div class="rounded-2xl bg-[#F6F5F2] px-3 py-2">逐段改写</div>
              <div class="rounded-2xl bg-[#F6F5F2] px-3 py-2">AI 痕迹与空泛检测</div>
              <div class="rounded-2xl bg-[#F6F5F2] px-3 py-2">推荐信草稿</div>
            </div>
            <button class="mt-6 w-full py-3 rounded-2xl px-4 text-sm font-medium transition-colors cursor-pointer bg-sage text-white hover:bg-sageDark">选择 Standard</button>
          </div>
          <div class="rounded-3xl bg-white shadow-sm ring-1 ring-stone-200 p-6">
            <div class="flex items-start justify-between gap-3">
              <div><div class="text-xl font-semibold text-textDark">Pro Review</div><div class="mt-2 text-3xl font-semibold text-textDark">¥699</div></div>
            </div>
            <div class="mt-3 text-sm leading-6 text-stone-600">适合需要更强交付质量的学生</div>
            <div class="mt-5 space-y-3 text-sm text-stone-700">
              <div class="rounded-2xl bg-[#F6F5F2] px-3 py-2">无限版本</div>
              <div class="rounded-2xl bg-[#F6F5F2] px-3 py-2">顾问 review 入口</div>
              <div class="rounded-2xl bg-[#F6F5F2] px-3 py-2">精修建议</div>
              <div class="rounded-2xl bg-[#F6F5F2] px-3 py-2">优先支持</div>
            </div>
            <button class="mt-6 w-full py-3 rounded-2xl px-4 text-sm font-medium transition-colors cursor-pointer border border-stone-200 text-stone-700 hover:bg-stone-50">选择 Pro Review</button>
          </div>
        </div>
      </section>
    </div>

  </main>

  <script>
    function navigate(pageId) {
      const pages = document.querySelectorAll('.page-section');
      pages.forEach(page => page.classList.add('hidden'));

      const targetPage = document.getElementById(`page-${pageId}`);
      if (targetPage) {
        targetPage.classList.remove('hidden');
      }

      const navButtons = document.querySelectorAll('.nav-btn');
      navButtons.forEach(btn => {
        if (btn.dataset.target === pageId) {
          btn.className = "nav-btn rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer bg-sage text-white hover:bg-sageDark";
        } else {
          btn.className = "nav-btn rounded-2xl px-4 py-2 text-sm font-medium transition-colors cursor-pointer text-stone-600 hover:bg-stone-100";
        }
      });
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }
  </script>
</body>
</html>
