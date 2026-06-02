<script setup>
import { ref } from "vue";

const mobileMenuOpen = ref(false);
const copied = ref(false);

const navItems = [
  { label: "概览", href: "#home" },
  { label: "技能", href: "#skills" },
  { label: "经历", href: "#experience" },
  { label: "项目", href: "#projects" },
  { label: "教育", href: "#education" }
];

const summary = [
  "5年 Java 全栈开发经验，主要做企业级中后台、流程型业务系统和数据类系统。",
  "后端以 Spring Boot、Spring Cloud、MySQL、Redis 为主，能承担 Vue、React 中后台页面开发与联调。",
  "做事风格偏扎实，不过度包装，更重视需求理解、系统稳定性和长期可维护性。",
  "习惯先梳理业务边界、状态流转和异常场景，再决定实现方式，适合复杂但需要稳妥推进的项目。"
];

const topMetrics = [
  { label: "工作经验", value: "5年" },
  { label: "主方向", value: "Java 全栈" },
  { label: "主要场景", value: "企业级中后台" }
];

const coreHighlights = [
  {
    title: "独立交付能力",
    text: "能够独立负责一个业务模块从需求理解、表结构设计、接口开发、前端联调到上线支持的完整流程。"
  },
  {
    title: "业务抽象能力",
    text: "对订单状态流转、权限边界、审批流程、异常补偿和日志追踪这类真实业务问题有持续积累。"
  },
  {
    title: "协作推进能力",
    text: "能与产品、测试、实施、运营配合推进复杂需求，接受反复沟通和场景收敛，不回避细节问题。"
  }
];

const achievementCards = [
  {
    title: "复杂流程落地",
    points: [
      "持续参与订单、审批、库存、工单、营销等多状态业务系统开发。",
      "对状态流转、异常处理、日志追踪、权限边界等高频问题有较多实战积累。"
    ]
  },
  {
    title: "前后端一体协同",
    points: [
      "不仅做后端接口，也能承担 Vue / React 中后台页面开发和复杂表单联调。",
      "在资源有限或节奏紧张的项目里，能直接补位页面实现与上线支持。"
    ]
  },
  {
    title: "稳定交付意识",
    points: [
      "关注接口幂等、缓存一致性、消息异步、补偿逻辑和上线后问题回溯。",
      "更倾向用简单稳妥的方式把需求交付，而不是为了复杂而复杂。"
    ]
  }
];

const skillMatrix = [
  {
    title: "Java / Spring 体系",
    icon: "backend",
    level: 88,
    note: "作为主要开发方向，能独立承担核心业务模块开发与维护。"
  },
  {
    title: "数据库设计与 SQL",
    icon: "database",
    level: 83,
    note: "能完成常规表结构设计、索引优化、复杂查询和数据问题排查。"
  },
  {
    title: "Redis / 消息队列",
    icon: "middleware",
    level: 78,
    note: "常用于缓存、异步解耦、状态同步和高频场景削峰。"
  },
  {
    title: "Spring Cloud 微服务",
    icon: "cloud",
    level: 80,
    note: "能参与微服务拆分、注册发现、配置管理、网关与服务调用链开发。"
  },
  {
    title: "Vue 中后台开发",
    icon: "frontend",
    level: 80,
    note: "可独立完成管理端页面、复杂表单、权限菜单和接口联调。"
  },
  {
    title: "React 中后台开发",
    icon: "react",
    level: 72,
    note: "可维护既有中后台项目并承担常规模块开发。"
  },
  {
    title: "问题排查与上线支持",
    icon: "ops",
    level: 84,
    note: "熟悉日志定位、接口排查、联调沟通和上线后问题跟进。"
  },
  {
    title: "工程化与部署协作",
    icon: "deploy",
    level: 76,
    note: "具备日常 Linux、Docker、Jenkins、Nginx 配置与发布配合经验。"
  }
];

const skillGroups = [
  {
    title: "后端开发",
    items: [
      "Java",
      "Spring Boot",
      "Spring Cloud",
      "Spring Cloud Alibaba",
      "Spring MVC",
      "Spring Security",
      "MyBatis / MyBatis-Plus",
      "JPA",
      "Hibernate",
      "OpenFeign",
      "Gateway",
      "Lombok",
      "MapStruct"
    ]
  },
  {
    title: "数据与中间件",
    items: [
      "MySQL",
      "SQL 优化",
      "Redis",
      "RabbitMQ",
      "Kafka",
      "Elasticsearch",
      "Nacos",
      "MinIO",
      "XXL-JOB",
      "Quartz",
      "Sentinel",
      "Seata"
    ]
  },
  {
    title: "前端能力",
    items: [
      "Vue 3",
      "Vue Router",
      "Pinia",
      "Element Plus",
      "ECharts",
      "JavaScript",
      "TypeScript",
      "HTML5",
      "CSS3",
      "React",
      "Ant Design",
      "Vite",
      "Axios"
    ]
  },
  {
    title: "工程协作",
    items: [
      "Maven",
      "Git",
      "GitLab",
      "Linux",
      "Docker",
      "Docker Compose",
      "Nginx",
      "Jenkins",
      "Swagger / OpenAPI",
      "JUnit",
      "Postman",
      "接口联调",
      "日志排查",
      "上线支持"
    ]
  },
  {
    title: "业务与架构实践",
    items: [
      "RBAC 权限模型",
      "审批流程",
      "订单状态流转",
      "异常补偿",
      "幂等处理",
      "缓存设计",
      "消息异步解耦",
      "多租户隔离"
    ]
  }
];

const experiences = [
  {
    period: "2023.01 - 至今",
    title: "Java 全栈工程师",
    company: "企业数字化服务公司",
    systems: [
      "供应链订单协同平台",
      "设备运维与工单 SaaS",
      "权限审批与报表分析系统"
    ],
    modules: [
      "订单中心",
      "库存占用",
      "工单流转",
      "设备台账",
      "Vue 中后台页面",
      "接口联调与上线支持"
    ],
    issues: [
      "复杂状态流转下的数据一致性与异常追踪",
      "跨角色、多流程场景下的权限边界控制",
      "多系统协作中的联调效率和上线后问题回溯"
    ],
    bullets: [
      "参与供应链协同、设备运维、权限流程、报表分析等企业级系统建设。",
      "负责核心业务模块设计与开发，同时承担部分 Vue 中后台页面、复杂表单流程和接口联调。",
      "日常工作更偏向需求拆解、状态流转梳理、异常场景补齐和上线问题排查。",
      "在多人协作场景中，持续负责接口文档维护、测试联调支持和线上问题复盘。"
    ]
  },
  {
    period: "2021.03 - 2022.12",
    title: "Java 开发工程师",
    company: "零售数字化项目团队",
    systems: [
      "会员商城",
      "营销运营后台",
      "订单中心与运营报表"
    ],
    modules: [
      "商品服务",
      "订单链路",
      "优惠券核销",
      "积分变更",
      "React 运营后台",
      "活动配置与联调支持"
    ],
    issues: [
      "高频活动场景下的幂等处理与异常补偿",
      "优惠券、积分、订单之间的状态一致性",
      "需求快速迭代时的回归验证与线上问题定位"
    ],
    bullets: [
      "参与会员商城、营销后台、订单中心、运营报表等模块开发与维护。",
      "积累了缓存使用、幂等处理、异常补偿、权限控制、上线支持等一线业务开发经验。",
      "从纯后端开发逐步延伸到 React / Vue 中后台页面开发，形成较完整的全栈交付能力。",
      "在需求迭代频繁的项目里，负责过多轮活动上线前检查、回归联调和异常订单问题跟进。"
    ]
  }
];

const projects = [
  {
    name: "供应链订单协同平台",
    period: "2024.03 - 2025.02",
    role: "Java 全栈工程师",
    stack: ["Spring Boot", "Spring Cloud", "MySQL", "Redis", "RabbitMQ", "Vue 3", "Element Plus"],
    background:
      "服务于制造企业与经销商协同场景，覆盖订单录入、采购申请、库存占用、发货跟踪、对账结算和异常处理。改造前同一笔业务需要在旧系统和 Excel 之间反复流转，状态不统一，改单和追溯成本都很高。",
    modules: [
      "订单中心",
      "库存占用",
      "审批流对接",
      "经销商门户",
      "操作日志"
    ],
    roleDetail: "负责后端核心链路开发，并承担经销商端页面改造与联调。",
    duties: [
      "负责订单中心、库存占用、审批流对接，以及经销商门户部分前端页面开发。",
      "将订单处理拆分为下单、审核、库存校验、出库通知、对账回写等职责更清晰的环节，通过消息队列降低同步耦合。",
      "设计订单状态机、操作日志和变更记录结构，覆盖撤单、驳回、补货、改地址、部分发货等真实场景。",
      "使用 Vue 3 + Element Plus 重做经销商端页面，补齐查询筛选、批量导出、审批进度展示和异常提醒。"
    ],
    result: [
      "订单流转效率明显提升，原先大量依赖人工沟通和表格确认的环节被系统化。",
      "库存误占、重复出库和状态不一致问题减少，客服与财务排查效率提升。",
      "业务链路可追踪后，问题定位方式从“找人问”转成“查日志和节点状态”。"
    ],
    gains: "对复杂状态流转、跨角色协作、库存与订单一致性这类业务问题有了更系统的落地经验。",
    keywords: [
      "订单状态机",
      "库存一致性",
      "消息异步解耦",
      "审批流对接",
      "操作日志追踪",
      "前后端联调"
    ]
  },
  {
    name: "设备运维与工单 SaaS 平台",
    period: "2023.04 - 2024.01",
    role: "后端主力开发 / 前端协同",
    stack: ["Spring Boot", "MyBatis-Plus", "Redis", "XXL-JOB", "Vue 3", "ECharts"],
    background:
      "项目面向连锁门店和区域服务团队，管理设备档案、巡检计划、故障报修、工单派发、备件申请、维修回访和费用结算。难点在于不同客户流程相近但细节差异明显，还需要支持多租户和多角色权限。",
    modules: [
      "工单中心",
      "设备台账",
      "巡检任务",
      "派单规则",
      "统计看板"
    ],
    roleDetail: "以工单与设备管理模块为主，兼顾流程配置、提醒能力和前端看板。",
    duties: [
      "主导工单模块、设备台账、派单规则、巡检任务和租户数据隔离方案的实现。",
      "抽象较轻量的流程配置能力，支持节点审批、回退、转派、超时提醒，避免为每个客户维护一套分支逻辑。",
      "结合定时任务和消息通知实现巡检提醒、超时工单催办、备件到货通知，减少人工盯单。",
      "参与前端开发，完成运维看板、工单列表、设备详情、统计图表和权限菜单联动。"
    ],
    result: [
      "平台能够较快复制到新客户场景，交付效率更高。",
      "工单流转更透明，设备数据和维修记录沉淀后，后续统计分析基础更完整。",
      "现场服务团队和后台协作效率提升，超时问题更容易被及时发现。"
    ],
    gains: "对多租户场景、流程可配置能力和工单系统的交付边界有了更清楚的理解。",
    keywords: [
      "多租户隔离",
      "工单状态流转",
      "流程可配置",
      "定时任务提醒",
      "权限边界控制",
      "统计看板联动"
    ]
  },
  {
    name: "会员商城与营销运营后台",
    period: "2021.05 - 2023.01",
    role: "Java 开发工程师",
    stack: ["Spring Boot", "Spring Cloud", "MySQL", "Redis", "Nacos", "React", "Ant Design"],
    background:
      "项目服务于会员商城与营销活动运营，包含商品、购物车、订单、优惠券、积分、活动规则和运营后台。业务特点是需求变化快、活动节奏密集，既要支持运营快速配置，也要尽量减少高峰期重复下单和优惠券状态异常。",
    modules: [
      "商品服务",
      "订单中心",
      "优惠券核销",
      "积分变更",
      "运营后台"
    ],
    roleDetail: "参与商城核心交易链路开发，并负责部分 React 运营后台页面维护。",
    duties: [
      "参与商品、订单、优惠券核销、积分变更、营销规则配置等模块开发。",
      "对关键下单链路补充参数校验、幂等处理和异常补偿，降低高峰期重复提交与数据不一致问题。",
      "维护 React 中后台页面，负责活动配置、券批次管理、商品审核和运营报表页面开发与联调。",
      "参与接口文档维护、测试联调和上线支持，协助产品与测试梳理边界场景。"
    ],
    result: [
      "活动配置流程更清晰，运营可以独立完成多数常规活动配置。",
      "高峰期重复下单和券状态异常问题减少，线上排障成本降低。",
      "后台页面稳定性和可用性提升后，客服和运营处理效率更平稳。"
    ],
    gains: "在高频迭代项目中积累了活动链路稳定性保障、订单问题排查和前后端协同的实战经验。",
    keywords: [
      "订单链路稳定性",
      "幂等处理",
      "优惠券状态一致性",
      "活动配置后台",
      "异常补偿",
      "高频迭代联调"
    ]
  }
];

async function copyEmail() {
  try {
    await navigator.clipboard.writeText("1796249008@qq.com");
    copied.value = true;
    window.setTimeout(() => {
      copied.value = false;
    }, 1800);
  } catch {
    copied.value = false;
  }
}

function closeMenu() {
  mobileMenuOpen.value = false;
}
</script>

<template>
  <div class="resume-page">
    <div class="backdrop-grid"></div>
    <div class="backdrop-glow glow-a"></div>
    <div class="backdrop-glow glow-b"></div>

    <header class="site-header">
      <div class="container header-inner">
        <a class="brand" href="#home">LIU WEI</a>

        <button
          class="nav-toggle"
          type="button"
          aria-label="切换导航"
          :aria-expanded="mobileMenuOpen ? 'true' : 'false'"
          @click="mobileMenuOpen = !mobileMenuOpen"
        >
          <span></span>
          <span></span>
        </button>

        <nav :class="['site-nav', { open: mobileMenuOpen }]">
          <a v-for="item in navItems" :key="item.href" :href="item.href" @click="closeMenu">
            {{ item.label }}
          </a>
        </nav>
      </div>
    </header>

    <main class="container main-shell">
      <section id="home" class="hero-panel">
        <div class="hero-main">
          <p class="eyebrow">JAVA FULL STACK RESUME</p>
          <h1>刘威</h1>
          <p class="hero-role">Java 全栈工程师</p>
          <p class="hero-intro">
            1997年，来自江西，毕业于江西师范大学，5年开发经验。主要做 Java 全栈方向，
            后端以 Spring Boot、Spring Cloud、MySQL、Redis 为主，前端可承担 Vue、React
            中后台页面开发与接口联调。
          </p>

          <div class="hero-tags">
            <span>5年经验</span>
            <span>Spring Boot</span>
            <span>Spring Cloud</span>
            <span>Vue</span>
            <span>React</span>
            <span>企业级中后台</span>
          </div>

          <div class="metric-strip">
            <div v-for="item in topMetrics" :key="item.label" class="metric-item">
              <span>{{ item.label }}</span>
              <strong>{{ item.value }}</strong>
            </div>
          </div>
        </div>

        <aside class="hero-aside">
          <div class="meta-card">
            <div class="meta-card-head">
              <span class="meta-dot"></span>
              <span>RESUME PROFILE</span>
            </div>
            <div class="meta-row">
              <span>邮箱</span>
              <strong>1796249008@qq.com</strong>
            </div>
            <div class="meta-row">
              <span>电话</span>
              <strong>15083632359</strong>
            </div>
            <div class="meta-row">
              <span>GitHub</span>
              <strong>github.com/GuiltyConscience</strong>
            </div>
            <div class="meta-row">
              <span>求职方向</span>
              <strong>Java 全栈 / 企业应用开发</strong>
            </div>
          </div>

          <div class="action-row">
            <a class="action-button primary" href="mailto:1796249008@qq.com">发送邮件</a>
            <button class="action-button secondary" type="button" @click="copyEmail">
              {{ copied ? "邮箱已复制" : "复制邮箱" }}
            </button>
          </div>
        </aside>
      </section>

      <section class="content-grid">
        <div class="left-column">
          <section class="section-card">
            <div class="section-head">
              <p class="eyebrow">SUMMARY</p>
              <h2>职业概述</h2>
            </div>
            <ul class="summary-list">
              <li v-for="item in summary" :key="item">{{ item }}</li>
            </ul>

            <div class="highlight-grid">
              <article v-for="item in coreHighlights" :key="item.title" class="highlight-item">
                <h3>{{ item.title }}</h3>
                <p>{{ item.text }}</p>
              </article>
            </div>
          </section>

          <section class="section-card">
            <div class="section-head">
              <p class="eyebrow">ACHIEVEMENTS</p>
              <h2>工作成果 / 核心亮点</h2>
            </div>

            <div class="achievement-grid">
              <article v-for="item in achievementCards" :key="item.title" class="achievement-card">
                <h3>{{ item.title }}</h3>
                <ul class="detail-list">
                  <li v-for="point in item.points" :key="point">{{ point }}</li>
                </ul>
              </article>
            </div>
          </section>

          <section id="experience" class="section-card">
            <div class="section-head">
              <p class="eyebrow">EXPERIENCE</p>
              <h2>工作经历</h2>
            </div>

            <div class="timeline-list">
              <article v-for="item in experiences" :key="item.period" class="timeline-item">
                <div class="item-top">
                  <div>
                    <p class="item-period">{{ item.period }}</p>
                    <h3>{{ item.title }}</h3>
                    <p class="item-company">{{ item.company }}</p>
                  </div>
                </div>

                <div class="experience-panels">
                  <section class="experience-panel">
                    <h4>负责系统</h4>
                    <div class="experience-tags">
                      <span v-for="system in item.systems" :key="system">{{ system }}</span>
                    </div>
                  </section>

                  <section class="experience-panel">
                    <h4>核心模块</h4>
                    <div class="experience-tags">
                      <span v-for="module in item.modules" :key="module">{{ module }}</span>
                    </div>
                  </section>

                  <section class="experience-panel">
                    <h4>关键问题</h4>
                    <ul class="detail-list compact-list">
                      <li v-for="issue in item.issues" :key="issue">{{ issue }}</li>
                    </ul>
                  </section>
                </div>

                <ul class="detail-list">
                  <li v-for="bullet in item.bullets" :key="bullet">{{ bullet }}</li>
                </ul>
              </article>
            </div>
          </section>
        </div>

        <div class="right-column">
          <section id="skills" class="section-card">
            <div class="section-head">
              <p class="eyebrow">SKILLS</p>
              <h2>核心技能</h2>
              <p class="section-desc">
                以下按实际使用频率和熟悉度整理，尽量覆盖目前工作中会长期使用到的技术栈与工程实践。
              </p>
            </div>

            <div class="skill-matrix">
              <article v-for="item in skillMatrix" :key="item.title" class="skill-meter">
                <div class="skill-meter-top">
                  <div class="skill-icon" :data-kind="item.icon">
                    <svg v-if="item.icon === 'backend'" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7">
                      <rect x="3" y="4" width="18" height="6" rx="2"></rect>
                      <rect x="3" y="14" width="18" height="6" rx="2"></rect>
                      <path d="M7 7h.01M7 17h.01"></path>
                    </svg>
                    <svg v-else-if="item.icon === 'database'" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7">
                      <ellipse cx="12" cy="5" rx="7" ry="3"></ellipse>
                      <path d="M5 5v14c0 1.66 3.13 3 7 3s7-1.34 7-3V5"></path>
                      <path d="M5 12c0 1.66 3.13 3 7 3s7-1.34 7-3"></path>
                    </svg>
                    <svg v-else-if="item.icon === 'middleware'" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7">
                      <path d="M6 8h12M6 16h12"></path>
                      <circle cx="8" cy="8" r="2"></circle>
                      <circle cx="16" cy="16" r="2"></circle>
                      <path d="M10 8h4M8 10v4M16 14V10"></path>
                    </svg>
                    <svg v-else-if="item.icon === 'cloud'" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7">
                      <path d="M7 18h10a4 4 0 0 0 .6-7.95A5.5 5.5 0 0 0 7 8.5 4.5 4.5 0 0 0 7 18z"></path>
                      <path d="M10 13h4M12 11v4"></path>
                    </svg>
                    <svg v-else-if="item.icon === 'frontend'" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7">
                      <rect x="3" y="4" width="18" height="14" rx="2"></rect>
                      <path d="M8 20h8M12 18v2"></path>
                      <path d="M10 9l-2 3 2 3M14 9l2 3-2 3"></path>
                    </svg>
                    <svg v-else-if="item.icon === 'react'" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7">
                      <circle cx="12" cy="12" r="1.4"></circle>
                      <ellipse cx="12" cy="12" rx="8" ry="3.2"></ellipse>
                      <ellipse cx="12" cy="12" rx="8" ry="3.2" transform="rotate(60 12 12)"></ellipse>
                      <ellipse cx="12" cy="12" rx="8" ry="3.2" transform="rotate(120 12 12)"></ellipse>
                    </svg>
                    <svg v-else-if="item.icon === 'deploy'" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7">
                      <path d="M4 7h16M4 12h16M4 17h10"></path>
                      <path d="M17 15l3 3-3 3"></path>
                    </svg>
                    <svg v-else viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7">
                      <path d="M12 3l7 4v5c0 4.5-2.8 7.8-7 9-4.2-1.2-7-4.5-7-9V7l7-4z"></path>
                      <path d="M9.5 12.5l1.7 1.7 3.6-4"></path>
                    </svg>
                  </div>
                  <div class="skill-meta">
                    <h3>{{ item.title }}</h3>
                    <span>{{ item.level }}%</span>
                  </div>
                </div>
                <div class="meter-track">
                  <div class="meter-fill" :style="{ width: item.level + '%' }"></div>
                </div>
                <p>{{ item.note }}</p>
              </article>
            </div>

            <div class="skill-groups">
              <article v-for="group in skillGroups" :key="group.title" class="skill-group">
                <h3>{{ group.title }}</h3>
                <div class="tag-list">
                  <span v-for="item in group.items" :key="item">{{ item }}</span>
                </div>
              </article>
            </div>
          </section>

          <section id="education" class="section-card">
            <div class="section-head">
              <p class="eyebrow">EDUCATION</p>
              <h2>教育背景</h2>
            </div>

            <div class="education-block">
              <p class="edu-school">江西师范大学</p>
              <p class="edu-meta">1997年生 · 江西 · 5年工作经验</p>
              <p class="edu-note">
                侧重企业应用和中后台系统开发，能够独立承担一个业务模块从需求理解、开发联调到上线支持的完整交付。
              </p>
            </div>
          </section>
        </div>
      </section>

      <section id="projects" class="section-card project-section">
        <div class="section-head">
          <p class="eyebrow">PROJECTS</p>
          <h2>项目经历</h2>
        </div>

        <div class="project-list">
          <article v-for="project in projects" :key="project.name" class="project-item">
            <div class="project-header">
              <div>
                <p class="item-period">{{ project.period }}</p>
                <h3>{{ project.name }}</h3>
                <p class="project-role-detail">{{ project.roleDetail }}</p>
              </div>
              <span class="role-badge">{{ project.role }}</span>
            </div>

            <div class="tag-list compact">
              <span v-for="item in project.stack" :key="item">{{ item }}</span>
            </div>

            <div class="module-list">
              <span v-for="item in project.modules" :key="item">{{ item }}</span>
            </div>

            <div class="keyword-block">
              <h4>技术难点关键词</h4>
              <div class="keyword-list">
                <span v-for="item in project.keywords" :key="item">{{ item }}</span>
              </div>
            </div>

            <div class="project-block">
              <h4>项目背景</h4>
              <p>{{ project.background }}</p>
            </div>

            <div class="project-columns">
              <section class="project-subcard">
                <h4>负责内容</h4>
                <ul class="detail-list">
                  <li v-for="item in project.duties" :key="item">{{ item }}</li>
                </ul>
              </section>
              <section class="project-subcard">
                <h4>项目结果</h4>
                <ul class="detail-list">
                  <li v-for="item in project.result" :key="item">{{ item }}</li>
                </ul>
              </section>
            </div>

            <div class="project-gain">
              <h4>项目收获</h4>
              <p>{{ project.gains }}</p>
            </div>
          </article>
        </div>
      </section>
    </main>
  </div>
</template>

<style scoped>
.resume-page {
  position: relative;
  min-height: 100vh;
  overflow: hidden;
}

.backdrop-grid {
  position: fixed;
  inset: 0;
  background-image:
    linear-gradient(rgba(148, 163, 184, 0.05) 1px, transparent 1px),
    linear-gradient(90deg, rgba(148, 163, 184, 0.05) 1px, transparent 1px);
  background-size: 36px 36px;
  mask-image: linear-gradient(180deg, rgba(0, 0, 0, 0.65), transparent 85%);
  pointer-events: none;
}

.backdrop-glow {
  position: fixed;
  border-radius: 999px;
  filter: blur(120px);
  pointer-events: none;
  opacity: 0.35;
}

.glow-a {
  top: -4rem;
  left: -6rem;
  width: 22rem;
  height: 22rem;
  background: rgba(34, 197, 94, 0.12);
}

.glow-b {
  top: 18rem;
  right: -5rem;
  width: 24rem;
  height: 24rem;
  background: rgba(59, 130, 246, 0.12);
}

.container {
  width: min(1200px, calc(100% - 32px));
  margin: 0 auto;
}

.site-header {
  position: sticky;
  top: 0;
  z-index: 20;
  backdrop-filter: blur(14px);
  background: rgba(7, 10, 18, 0.72);
  border-bottom: 1px solid rgba(148, 163, 184, 0.08);
}

.header-inner {
  position: relative;
  min-height: 76px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 24px;
}

.brand,
.eyebrow,
.item-period {
  font-family: "JetBrains Mono", monospace;
}

.brand {
  color: #f8fafc;
  font-size: 0.98rem;
  font-weight: 700;
  letter-spacing: 0.22em;
}

.site-nav {
  display: flex;
  align-items: center;
  gap: 8px;
}

.site-nav a {
  min-height: 44px;
  display: inline-flex;
  align-items: center;
  padding: 0 14px;
  border-radius: 999px;
  color: #94a3b8;
  transition: 180ms ease;
}

.site-nav a:hover {
  color: #f8fafc;
  background: rgba(255, 255, 255, 0.06);
}

.nav-toggle {
  display: none;
  width: 48px;
  height: 48px;
  position: relative;
  border: 0;
  border-radius: 14px;
  background: rgba(255, 255, 255, 0.05);
}

.nav-toggle span {
  position: absolute;
  left: 13px;
  width: 22px;
  height: 2px;
  border-radius: 999px;
  background: #e2e8f0;
}

.nav-toggle span:first-child {
  top: 18px;
}

.nav-toggle span:last-child {
  top: 28px;
}

.main-shell {
  position: relative;
  z-index: 1;
  padding: 28px 0 56px;
}

.hero-panel,
.section-card {
  background: linear-gradient(180deg, rgba(15, 23, 42, 0.92), rgba(10, 15, 28, 0.9));
  border: 1px solid rgba(148, 163, 184, 0.12);
  box-shadow: 0 24px 60px rgba(0, 0, 0, 0.28);
}

.hero-panel {
  display: grid;
  grid-template-columns: minmax(0, 1.2fr) minmax(320px, 0.8fr);
  gap: 24px;
  padding: 36px;
  border-radius: 32px;
  position: relative;
  overflow: hidden;
}

.hero-panel::before {
  content: "";
  position: absolute;
  inset: 0;
  background:
    radial-gradient(circle at top right, rgba(56, 189, 248, 0.12), transparent 30%),
    linear-gradient(135deg, rgba(255, 255, 255, 0.02), transparent 50%);
  pointer-events: none;
}

.eyebrow {
  margin: 0 0 12px;
  font-size: 0.76rem;
  letter-spacing: 0.18em;
  color: #38bdf8;
}

h1,
h2,
h3,
h4 {
  margin: 0;
  color: #f8fafc;
  font-family: "Outfit", "Noto Sans SC", sans-serif;
  letter-spacing: -0.03em;
}

h1 {
  font-size: clamp(3.1rem, 6vw, 5.2rem);
  line-height: 0.94;
}

.hero-role {
  margin: 14px 0 0;
  font-size: 1.16rem;
  color: #38bdf8;
  font-weight: 600;
}

.hero-intro,
.project-block p,
.education-block p {
  margin: 18px 0 0;
  color: #cbd5e1;
  line-height: 1.9;
}

.hero-tags,
.tag-list {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}

.hero-tags {
  margin-top: 22px;
}

.hero-tags span,
.tag-list span {
  border-radius: 999px;
  border: 1px solid rgba(148, 163, 184, 0.16);
  background: rgba(15, 23, 42, 0.9);
  color: #dbeafe;
  padding: 8px 12px;
  font-size: 0.84rem;
}

.hero-aside {
  display: grid;
  gap: 16px;
}

.metric-strip {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 12px;
  margin-top: 24px;
}

.metric-item {
  padding: 14px 16px;
  border-radius: 18px;
  background: rgba(2, 6, 23, 0.5);
  border: 1px solid rgba(148, 163, 184, 0.1);
}

.metric-item span {
  display: block;
  color: #94a3b8;
  font-size: 0.8rem;
}

.metric-item strong {
  display: block;
  margin-top: 8px;
  color: #f8fafc;
  font-size: 1rem;
}

.meta-card {
  padding: 20px;
  border-radius: 24px;
  background: rgba(2, 6, 23, 0.76);
  border: 1px solid rgba(148, 163, 184, 0.1);
}

.meta-card-head {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 6px;
  color: #7dd3fc;
  font-family: "JetBrains Mono", monospace;
  font-size: 0.76rem;
  letter-spacing: 0.12em;
}

.meta-dot {
  width: 8px;
  height: 8px;
  border-radius: 999px;
  background: #22c55e;
  box-shadow: 0 0 0 6px rgba(34, 197, 94, 0.12);
}

.meta-row {
  display: flex;
  justify-content: space-between;
  gap: 16px;
  padding: 14px 0;
  border-bottom: 1px solid rgba(148, 163, 184, 0.08);
}

.meta-row:last-child {
  border-bottom: 0;
}

.meta-row span {
  color: #94a3b8;
}

.meta-row strong {
  color: #f8fafc;
  text-align: right;
}

.action-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 12px;
}

.action-button {
  min-height: 46px;
  border-radius: 16px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  font-weight: 600;
  cursor: pointer;
  transition: transform 180ms ease, background 180ms ease, border-color 180ms ease;
}

.action-button:hover {
  transform: translateY(-1px);
}

.action-button.primary {
  background: linear-gradient(135deg, #0ea5e9, #2563eb);
  color: #eff6ff;
  border: 1px solid transparent;
}

.action-button.secondary {
  background: rgba(255, 255, 255, 0.04);
  color: #e2e8f0;
  border: 1px solid rgba(148, 163, 184, 0.14);
}

.content-grid {
  display: grid;
  grid-template-columns: minmax(0, 1.2fr) minmax(320px, 0.8fr);
  gap: 20px;
  margin-top: 20px;
}

.left-column,
.right-column,
.project-list,
.timeline-list,
.skill-groups {
  display: grid;
  gap: 20px;
}

.section-card {
  padding: 28px;
  border-radius: 28px;
}

.section-head {
  margin-bottom: 18px;
}

.section-head h2 {
  font-size: clamp(1.65rem, 3vw, 2.5rem);
}

.section-desc {
  margin: 10px 0 0;
  color: #94a3b8;
  line-height: 1.8;
}

.summary-list,
.detail-list {
  margin: 0;
  padding: 0;
  list-style: none;
}

.summary-list {
  display: grid;
  gap: 14px;
}

.summary-list li,
.detail-list li,
.edu-note {
  position: relative;
  padding-left: 18px;
  color: #cbd5e1;
  line-height: 1.82;
}

.highlight-grid {
  display: grid;
  gap: 14px;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  margin-top: 24px;
}

.highlight-item {
  padding: 18px;
  border-radius: 18px;
  background: rgba(2, 6, 23, 0.52);
  border: 1px solid rgba(148, 163, 184, 0.1);
}

.highlight-item h3 {
  font-size: 1rem;
}

.highlight-item p,
.skill-meter p,
.project-gain p {
  margin: 10px 0 0;
  color: #94a3b8;
  line-height: 1.78;
}

.achievement-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 14px;
}

.achievement-card {
  padding: 18px;
  border-radius: 18px;
  background: linear-gradient(180deg, rgba(2, 6, 23, 0.62), rgba(15, 23, 42, 0.44));
  border: 1px solid rgba(148, 163, 184, 0.1);
}

.achievement-card h3 {
  margin-bottom: 12px;
  font-size: 1rem;
}

.summary-list li::before,
.detail-list li::before {
  content: "";
  position: absolute;
  left: 0;
  top: 12px;
  width: 6px;
  height: 6px;
  border-radius: 999px;
  background: #38bdf8;
  box-shadow: 0 0 0 5px rgba(56, 189, 248, 0.1);
}

.timeline-item,
.project-item,
.skill-group {
  border-radius: 22px;
  background: rgba(2, 6, 23, 0.55);
  border: 1px solid rgba(148, 163, 184, 0.1);
}

.skill-matrix {
  display: grid;
  gap: 14px;
  margin-bottom: 20px;
}

.skill-meter {
  padding: 16px;
  border-radius: 20px;
  background: rgba(2, 6, 23, 0.5);
  border: 1px solid rgba(148, 163, 184, 0.1);
  position: relative;
  overflow: hidden;
}

.skill-meter::before {
  content: "";
  position: absolute;
  inset: 0 auto 0 0;
  width: 3px;
  background: linear-gradient(180deg, #38bdf8, #22c55e);
}

.skill-meter-top {
  display: flex;
  align-items: center;
  gap: 12px;
}

.skill-icon {
  width: 40px;
  height: 40px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border-radius: 12px;
  background: rgba(37, 99, 235, 0.12);
  color: #7dd3fc;
  flex-shrink: 0;
}

.skill-icon svg {
  width: 22px;
  height: 22px;
}

.skill-meta {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 12px;
  width: 100%;
}

.skill-meta h3 {
  font-size: 1rem;
}

.skill-meta span {
  color: #dbeafe;
  font-family: "JetBrains Mono", monospace;
  font-size: 0.86rem;
}

.meter-track {
  width: 100%;
  height: 8px;
  border-radius: 999px;
  background: rgba(148, 163, 184, 0.12);
  margin-top: 14px;
  overflow: hidden;
}

.meter-fill {
  height: 100%;
  border-radius: 999px;
  background: linear-gradient(90deg, #0ea5e9 0%, #2563eb 60%, #22c55e 100%);
}

.timeline-item {
  padding: 22px;
}

.experience-panels {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 14px;
  margin-bottom: 16px;
}

.experience-panel {
  padding: 16px;
  border-radius: 18px;
  background: rgba(15, 23, 42, 0.58);
  border: 1px solid rgba(148, 163, 184, 0.08);
}

.experience-panel h4 {
  color: #e2e8f0;
  font-size: 0.94rem;
}

.experience-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 12px;
}

.experience-tags span {
  border-radius: 10px;
  padding: 8px 10px;
  background: rgba(2, 6, 23, 0.7);
  border: 1px solid rgba(148, 163, 184, 0.08);
  color: #cbd5e1;
  font-size: 0.82rem;
}

.compact-list {
  margin-top: 12px;
}

.compact-list li {
  line-height: 1.72;
}

.item-top {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 16px;
  margin-bottom: 12px;
}

.item-period {
  margin: 0 0 10px;
  font-size: 0.78rem;
  letter-spacing: 0.08em;
  color: #38bdf8;
}

.item-company {
  margin: 8px 0 0;
  color: #94a3b8;
}

.skill-group {
  padding: 18px;
}

.skill-group h3 {
  margin-bottom: 14px;
  font-size: 1.02rem;
}

.education-block {
  border-radius: 22px;
  background: rgba(2, 6, 23, 0.55);
  border: 1px solid rgba(148, 163, 184, 0.1);
  padding: 20px;
}

.edu-school {
  margin: 0;
  font-size: 1.08rem;
  color: #f8fafc;
  font-weight: 700;
}

.edu-meta {
  margin-top: 10px;
  color: #94a3b8;
}

.edu-note {
  margin-top: 14px;
}

.project-section {
  margin-top: 20px;
}

.project-item {
  padding: 24px;
  position: relative;
  overflow: hidden;
}

.project-item::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 1px;
  background: linear-gradient(90deg, rgba(56, 189, 248, 0.5), transparent 55%);
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 16px;
}

.role-badge {
  white-space: nowrap;
  color: #dbeafe;
  background: rgba(37, 99, 235, 0.16);
  border: 1px solid rgba(96, 165, 250, 0.16);
  border-radius: 999px;
  padding: 8px 12px;
  font-size: 0.84rem;
}

.project-role-detail {
  margin: 10px 0 0;
  color: #94a3b8;
}

.tag-list.compact {
  margin-top: 14px;
}

.module-list {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 14px;
}

.module-list span {
  border-radius: 10px;
  padding: 8px 10px;
  background: rgba(15, 23, 42, 0.78);
  border: 1px solid rgba(148, 163, 184, 0.08);
  color: #cbd5e1;
  font-size: 0.82rem;
}

.keyword-list {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 10px;
}

.keyword-block {
  margin-top: 16px;
}

.keyword-block h4 {
  color: #e2e8f0;
  font-size: 0.96rem;
}

.keyword-list span {
  color: #7dd3fc;
  font-size: 0.82rem;
  padding: 0;
}

.keyword-list span::before {
  content: "#";
  margin-right: 2px;
  color: #38bdf8;
}

.project-block {
  margin-top: 18px;
}

.project-block h4,
.project-subcard h4 {
  color: #e2e8f0;
  font-size: 0.96rem;
}

.project-columns {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
  margin-top: 18px;
}

.project-subcard {
  padding: 18px;
  border-radius: 20px;
  background: rgba(15, 23, 42, 0.72);
  border: 1px solid rgba(148, 163, 184, 0.1);
}

.project-subcard .detail-list {
  margin-top: 12px;
}

.project-gain {
  margin-top: 18px;
  padding-top: 18px;
  border-top: 1px solid rgba(148, 163, 184, 0.08);
}

.project-gain h4 {
  color: #e2e8f0;
  font-size: 0.96rem;
}

@media (max-width: 1040px) {
  .hero-panel,
  .content-grid,
  .project-columns {
    grid-template-columns: 1fr;
  }

  .highlight-grid,
  .achievement-grid,
  .metric-strip {
    grid-template-columns: 1fr;
  }

  .experience-panels {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 760px) {
  .container {
    width: min(1200px, calc(100% - 20px));
  }

  .nav-toggle {
    display: inline-flex;
  }

  .site-nav {
    position: absolute;
    top: calc(100% + 10px);
    right: 0;
    left: 0;
    display: none;
    flex-direction: column;
    align-items: stretch;
    padding: 10px;
    border-radius: 20px;
    background: rgba(10, 15, 28, 0.96);
    border: 1px solid rgba(148, 163, 184, 0.12);
  }

  .site-nav.open {
    display: flex;
  }

  .site-nav a {
    justify-content: center;
  }

  .hero-panel,
  .section-card {
    padding: 20px 16px;
    border-radius: 24px;
  }

  .project-item,
  .timeline-item,
  .skill-group,
  .education-block,
  .meta-card {
    padding: 16px;
  }

  .action-row,
  .project-header,
  .meta-row {
    grid-template-columns: 1fr;
    flex-direction: column;
    align-items: flex-start;
  }

  .meta-row strong {
    text-align: left;
  }
}
</style>
