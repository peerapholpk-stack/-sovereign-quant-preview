<template>
  <div class="min-h-screen bg-white font-sans text-slate-900 antialiased">
    <!-- ============================================================ -->
    <!-- NAV                                                           -->
    <!-- ============================================================ -->
    <header class="sticky top-0 z-50 border-b border-slate-200/70 bg-white/80 backdrop-blur-xl">
      <div class="mx-auto flex h-14 max-w-6xl items-center justify-between px-6">
        <a href="#top" class="flex items-center gap-2 font-semibold tracking-tight">
          <span class="grid h-6 w-6 place-items-center rounded-md bg-slate-900 text-white">
            <Hexagon :size="14" :stroke-width="2.25" />
          </span>
          <span>SovereignQuant</span>
        </a>
        <nav class="hidden items-center gap-8 text-sm text-slate-600 md:flex">
          <a href="#product" class="transition hover:text-slate-900">Product</a>
          <a href="#capabilities" class="transition hover:text-slate-900">Capabilities</a>
          <a href="#strategies" class="transition hover:text-slate-900">Strategies</a>
          <a href="#architecture" class="transition hover:text-slate-900">Architecture</a>
          <a href="#pricing" class="transition hover:text-slate-900">Pricing</a>
        </nav>
        <a
          href="#pricing"
          class="group inline-flex items-center gap-1.5 rounded-md bg-slate-900 px-3.5 py-1.5 text-sm font-medium text-white shadow-soft transition hover:bg-slate-800"
        >
          Acquire
          <ArrowRight :size="14" :stroke-width="2.25" class="transition group-hover:translate-x-0.5" />
        </a>
      </div>
    </header>

    <!-- ============================================================ -->
    <!-- HERO + DASHBOARD MOCKUP                                       -->
    <!-- ============================================================ -->
    <section id="top" class="relative overflow-hidden">
      <div class="pointer-events-none absolute inset-0 grid-pattern opacity-60" aria-hidden="true" />
      <div
        class="pointer-events-none absolute left-1/2 top-20 h-72 w-[44rem] -translate-x-1/2 rounded-full bg-gradient-to-b from-indigo-100/60 to-transparent blur-3xl"
        aria-hidden="true"
      />

      <div class="relative mx-auto max-w-6xl px-6 pb-20 pt-20 sm:pt-28 lg:pb-24 lg:pt-32">
        <div class="mx-auto max-w-4xl text-center">
          <a
            href="#product"
            class="anim-fade-up anim-d-0 inline-flex items-center gap-2 rounded-full border border-slate-200 bg-white/80 px-3 py-1 text-xs font-medium text-slate-600 shadow-soft backdrop-blur transition hover:border-slate-300"
          >
            <span class="relative flex h-1.5 w-1.5">
              <span class="absolute inline-flex h-full w-full animate-ping rounded-full bg-emerald-400 opacity-75" />
              <span class="relative inline-flex h-1.5 w-1.5 rounded-full bg-emerald-500" />
            </span>
            <span>v1.0 · Self-hosted quant trading infrastructure</span>
          </a>

          <h1
            class="anim-fade-up anim-d-1 mt-6 text-balance text-5xl font-extrabold leading-[1.02] tracking-tight text-slate-900 sm:text-6xl lg:text-7xl"
          >
            Your Quant Bot.<br class="hidden sm:block" />
            Your Server. Your Edge.
          </h1>

          <p class="anim-fade-up anim-d-2 mx-auto mt-6 max-w-2xl text-balance text-lg leading-relaxed text-slate-600 sm:text-xl">
            A complete crypto futures trading stack — 14 built-in strategies,
            batch optimization with overfit detection, regime-aware execution,
            and a full monitoring dashboard. Deploy it once. Own the source
            forever.
          </p>

          <div class="anim-fade-up anim-d-3 mt-10 flex flex-col items-center justify-center gap-3 sm:flex-row sm:gap-4">
            <a
              href="#pricing"
              class="group inline-flex w-full items-center justify-center gap-2 rounded-lg bg-slate-900 px-6 py-3 text-sm font-semibold text-white shadow-soft transition hover:-translate-y-0.5 hover:bg-slate-800 hover:shadow-lg sm:w-auto"
            >
              Acquire Source Code
              <ArrowRight :size="16" :stroke-width="2.25" class="transition group-hover:translate-x-0.5" />
            </a>
            <a
              href="#architecture"
              class="inline-flex w-full items-center justify-center gap-2 rounded-lg border border-slate-300 bg-white px-6 py-3 text-sm font-semibold text-slate-900 transition hover:-translate-y-0.5 hover:border-slate-400 hover:bg-slate-50 sm:w-auto"
            >
              View Architecture
            </a>
          </div>
        </div>

        <!-- ====== DASHBOARD MOCKUP ====== -->
        <div id="product" class="anim-fade-up anim-d-4 relative mx-auto mt-16 w-full max-w-6xl">
          <div
            class="pointer-events-none absolute -inset-x-4 -inset-y-6 rounded-[2rem] bg-gradient-to-b from-slate-200/60 via-indigo-100/30 to-transparent blur-2xl"
            aria-hidden="true"
          />

          <!-- Browser chrome -->
          <div class="relative overflow-hidden rounded-2xl border border-slate-200 bg-white shadow-2xl shadow-slate-900/10 ring-1 ring-black/[0.02]">
            <div class="flex items-center gap-3 border-b border-slate-200 bg-slate-50/80 px-4 py-2.5">
              <div class="flex items-center gap-1.5">
                <span class="h-3 w-3 rounded-full bg-slate-300" />
                <span class="h-3 w-3 rounded-full bg-slate-300" />
                <span class="h-3 w-3 rounded-full bg-slate-300" />
              </div>
              <div class="flex flex-1 items-center justify-center">
                <div class="flex items-center gap-1.5 rounded-md border border-slate-200 bg-white px-2.5 py-1 font-mono text-[11px] font-medium text-slate-500">
                  <Lock :size="11" :stroke-width="2" />
                  localhost:3000 / dashboard
                </div>
              </div>
              <div class="flex items-center gap-1.5 font-mono text-[10px] font-medium text-slate-500">
                <span class="h-1.5 w-1.5 animate-pulse rounded-full bg-emerald-500" />
                <span class="hidden sm:inline">LIVE</span>
              </div>
            </div>

            <!-- Dashboard body (dark, matches real app) -->
            <div class="grid grid-cols-[56px_1fr] bg-zinc-950 text-zinc-100 sm:grid-cols-[180px_1fr]">
              <!-- Sidebar -->
              <aside class="flex flex-col border-r border-white/5 bg-zinc-950/90 py-4">
                <div class="mb-6 hidden px-4 sm:block">
                  <div class="flex items-center gap-2">
                    <span class="grid h-6 w-6 place-items-center rounded-md bg-blue-600 text-white">
                      <Hexagon :size="12" :stroke-width="2.25" />
                    </span>
                    <span class="text-sm font-semibold tracking-tight">SovereignQuant</span>
                  </div>
                </div>
                <nav class="space-y-0.5 px-2 text-[12px]">
                  <a
                    v-for="(item, i) in sidebar"
                    :key="item.label"
                    href="#"
                    :class="[
                      'flex items-center gap-2.5 rounded-md px-2.5 py-2 transition',
                      item.active
                        ? 'bg-blue-500/10 text-blue-300 ring-1 ring-inset ring-blue-500/20'
                        : 'text-zinc-400 hover:bg-white/[0.03] hover:text-zinc-200',
                    ]"
                    :style="{ animationDelay: (i * 60 + 400) + 'ms' }"
                  >
                    <component :is="item.icon" :size="14" :stroke-width="2" />
                    <span class="hidden sm:inline">{{ item.label }}</span>
                  </a>
                </nav>
                <div class="mt-auto hidden px-4 sm:block">
                  <div class="rounded-md border border-white/5 bg-white/[0.02] p-2.5">
                    <div class="flex items-center gap-2 text-[10px] font-mono text-zinc-400">
                      <span class="h-1.5 w-1.5 animate-pulse rounded-full bg-emerald-500" />
                      monitor · healthy
                    </div>
                    <div class="mt-1 font-mono text-[10px] text-zinc-500">pid 18342 · 5m scan</div>
                  </div>
                </div>
              </aside>

              <!-- Main content -->
              <div class="p-4 sm:p-6">
                <!-- Header -->
                <div class="flex items-end justify-between">
                  <div>
                    <h3 class="text-base font-bold tracking-tight text-white sm:text-lg">Performance Overview</h3>
                    <p class="mt-0.5 text-[11px] text-zinc-400 sm:text-xs">Bot status · last sync 2s ago</p>
                  </div>
                  <div class="flex gap-1.5 sm:gap-2">
                    <button class="rounded-md border border-white/10 bg-white/[0.03] px-2.5 py-1 text-[11px] font-medium text-zinc-300">
                      Export
                    </button>
                    <button class="rounded-md bg-blue-600 px-2.5 py-1 text-[11px] font-medium text-white shadow-[0_0_20px_rgba(37,99,235,0.4)]">
                      Manage Bot
                    </button>
                  </div>
                </div>

                <!-- KPI cards -->
                <div class="mt-4 grid grid-cols-2 gap-2 sm:gap-3 lg:grid-cols-4">
                  <div
                    v-for="(kpi, i) in kpis"
                    :key="kpi.label"
                    class="relative overflow-hidden rounded-xl border border-white/5 bg-white/[0.025] p-3 sm:p-4"
                  >
                    <div class="absolute right-3 top-3 text-blue-400/40">
                      <component :is="kpi.icon" :size="16" :stroke-width="2" />
                    </div>
                    <div class="text-[10px] font-medium text-zinc-400 sm:text-[11px]">{{ kpi.label }}</div>
                    <div
                      class="mt-1 font-mono text-lg font-bold tracking-tight text-white sm:text-xl"
                      :class="kpi.tick"
                    >
                      {{ kpi.value }}
                    </div>
                    <div
                      v-if="kpi.delta"
                      class="mt-1.5 flex items-center gap-1 text-[10px] font-medium"
                      :class="kpi.up ? 'text-emerald-400' : 'text-rose-400'"
                    >
                      <component :is="kpi.up ? ArrowUpRight : ArrowDownRight" :size="11" :stroke-width="2.5" />
                      {{ kpi.delta }}
                    </div>
                  </div>
                </div>

                <!-- Chart + Feed -->
                <div class="mt-3 grid grid-cols-1 gap-3 lg:grid-cols-3">
                  <!-- Equity Curve -->
                  <div class="lg:col-span-2 rounded-xl border border-white/5 bg-white/[0.025] p-3 sm:p-4">
                    <div class="flex items-center justify-between">
                      <h4 class="text-xs font-semibold tracking-wide text-white/90 sm:text-sm">Equity Curve</h4>
                      <div class="flex gap-0.5 rounded-md border border-white/5 bg-white/[0.03] p-0.5 text-[10px]">
                        <span v-for="r in ['1D','1W','1M','ALL']" :key="r"
                          :class="[
                            'rounded px-1.5 py-0.5 font-medium',
                            r === '1W' ? 'bg-white/10 text-white' : 'text-zinc-500',
                          ]"
                        >{{ r }}</span>
                      </div>
                    </div>

                    <div class="relative mt-3 h-36 w-full sm:h-44">
                      <!-- gridlines -->
                      <div class="pointer-events-none absolute inset-0 flex flex-col justify-between">
                        <div v-for="n in 4" :key="n" class="border-t border-dashed border-white/[0.05]" />
                      </div>

                      <svg viewBox="0 0 600 200" preserveAspectRatio="none" class="absolute inset-0 h-full w-full">
                        <defs>
                          <linearGradient id="eqFill" x1="0" x2="0" y1="0" y2="1">
                            <stop offset="0%" stop-color="#3b82f6" stop-opacity="0.35" />
                            <stop offset="100%" stop-color="#3b82f6" stop-opacity="0" />
                          </linearGradient>
                        </defs>
                        <!-- area -->
                        <path
                          class="equity-area"
                          :d="equityArea"
                          fill="url(#eqFill)"
                        />
                        <!-- line -->
                        <path
                          class="equity-line"
                          :d="equityPath"
                          fill="none"
                          stroke="#60a5fa"
                          stroke-width="2.25"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        />
                      </svg>

                      <!-- trailing dot -->
                      <span class="equity-dot absolute right-[4%] top-[12%] flex h-2.5 w-2.5">
                        <span class="absolute inline-flex h-full w-full animate-ping rounded-full bg-blue-400 opacity-70" />
                        <span class="relative inline-flex h-2.5 w-2.5 rounded-full border-2 border-white bg-blue-500" />
                      </span>
                    </div>

                    <!-- footer stats -->
                    <div class="mt-3 grid grid-cols-3 border-t border-white/5 pt-3 text-[10px] sm:text-[11px]">
                      <div>
                        <div class="text-zinc-500">Sharpe</div>
                        <div class="mt-0.5 font-mono font-semibold text-white">2.18</div>
                      </div>
                      <div>
                        <div class="text-zinc-500">Max DD</div>
                        <div class="mt-0.5 font-mono font-semibold text-white">-8.4%</div>
                      </div>
                      <div>
                        <div class="text-zinc-500">Expectancy</div>
                        <div class="mt-0.5 font-mono font-semibold text-emerald-400">+0.42R</div>
                      </div>
                    </div>
                  </div>

                  <!-- Recent Execution -->
                  <div class="rounded-xl border border-white/5 bg-white/[0.025] p-3 sm:p-4">
                    <h4 class="flex items-center gap-2 text-xs font-semibold tracking-wide text-white/90 sm:text-sm">
                      <span class="h-1.5 w-1.5 animate-pulse rounded-full bg-blue-500" />
                      Recent Execution
                    </h4>

                    <div class="mt-3 space-y-1.5">
                      <div
                        v-for="(t, i) in trades"
                        :key="i"
                        class="feed-row flex items-center justify-between rounded-md border border-transparent bg-white/[0.02] px-2.5 py-2"
                        :style="{ animationDelay: (i * 180 + 700) + 'ms' }"
                      >
                        <div class="min-w-0">
                          <div class="flex items-center gap-1.5">
                            <span
                              :class="[
                                'rounded-sm px-1.5 py-px text-[9px] font-bold tracking-wide',
                                t.side === 'LONG'
                                  ? 'bg-emerald-500/20 text-emerald-300'
                                  : 'bg-rose-500/20 text-rose-300',
                              ]"
                            >{{ t.side }}</span>
                            <span class="text-[11px] font-semibold text-white">{{ t.symbol }}</span>
                            <span class="text-[10px] text-zinc-500">{{ t.lev }}×</span>
                          </div>
                          <div class="mt-0.5 font-mono text-[10px] text-zinc-500">{{ t.time }}</div>
                        </div>
                        <div class="text-right">
                          <div class="font-mono text-[11px] text-white">{{ t.price }}</div>
                          <div
                            v-if="t.pnl"
                            :class="[
                              'font-mono text-[10px] font-semibold',
                              t.pnlUp ? 'text-emerald-400' : 'text-rose-400',
                            ]"
                          >{{ t.pnl }}</div>
                          <div v-else class="text-[10px] font-medium text-blue-400">OPEN</div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>

                <!-- Bottom console -->
                <div class="mt-3 flex flex-wrap items-center gap-x-4 gap-y-1 rounded-lg border border-white/5 bg-white/[0.02] px-3 py-2 font-mono text-[10px] text-zinc-500">
                  <span class="flex items-center gap-1.5"><span class="h-1.5 w-1.5 rounded-full bg-emerald-500" />worker healthy</span>
                  <span>regime: TREND_UP</span>
                  <span class="hidden sm:inline">MC sims: 10,000</span>
                  <span class="hidden md:inline">strategies: 14</span>
                  <span class="ml-auto">
                    <span class="text-emerald-400">▲ scan #1284 · 30 symbols</span>
                    <span class="ml-1 inline-block h-2.5 w-[5px] translate-y-[2px] bg-zinc-400 animate-blink align-middle" />
                  </span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Trust row -->
        <div class="anim-fade-up anim-d-5 mt-14 flex flex-wrap items-center justify-center gap-x-8 gap-y-3 text-xs font-medium uppercase tracking-wider text-slate-400">
          <span class="flex items-center gap-1.5"><Check :size="14" :stroke-width="2.5" /> FastAPI</span>
          <span class="flex items-center gap-1.5"><Check :size="14" :stroke-width="2.5" /> Next.js 15</span>
          <span class="flex items-center gap-1.5"><Check :size="14" :stroke-width="2.5" /> TimescaleDB</span>
          <span class="flex items-center gap-1.5"><Check :size="14" :stroke-width="2.5" /> Redis</span>
          <span class="flex items-center gap-1.5"><Check :size="14" :stroke-width="2.5" /> Docker</span>
          <span class="flex items-center gap-1.5"><Check :size="14" :stroke-width="2.5" /> CCXT Pro</span>
        </div>
      </div>
    </section>

    <!-- ============================================================ -->
    <!-- CORE CAPABILITIES                                             -->
    <!-- ============================================================ -->
    <section id="capabilities" class="border-t border-slate-200 bg-white">
      <div class="mx-auto max-w-6xl px-6 py-20 lg:py-28">
        <div v-reveal class="mx-auto max-w-2xl text-center">
          <p class="text-xs font-semibold uppercase tracking-[0.18em] text-indigo-600">What's Inside</p>
          <h2 class="mt-3 text-3xl font-bold tracking-tight text-slate-900 sm:text-4xl">
            A full trading stack — not a toolkit.
          </h2>
          <p class="mt-4 text-base text-slate-600">
            Strategy research, risk modeling, live execution, and monitoring
            ship as one coherent system you can actually run.
          </p>
        </div>

        <div class="mt-14 grid grid-cols-1 gap-px overflow-hidden rounded-xl border border-slate-200 bg-slate-200 md:grid-cols-3">
          <article
            v-for="(cap, i) in capabilities"
            :key="cap.title"
            v-reveal
            :style="{ '--reveal-delay': (i * 120) + 'ms' }"
            class="group relative flex flex-col gap-4 bg-white p-8 transition duration-300 hover:-translate-y-0.5 hover:bg-slate-50/60"
          >
            <div class="flex h-10 w-10 items-center justify-center rounded-lg border border-slate-200 bg-white text-slate-900 shadow-soft transition group-hover:border-slate-300 group-hover:shadow-md">
              <component :is="cap.icon" :size="18" :stroke-width="2" />
            </div>
            <h3 class="text-lg font-semibold tracking-tight text-slate-900">{{ cap.title }}</h3>
            <p class="text-sm leading-relaxed text-slate-600">{{ cap.description }}</p>
            <ul class="mt-1 space-y-1.5 text-sm text-slate-600">
              <li v-for="b in cap.bullets" :key="b" class="flex items-start gap-2">
                <Check :size="14" :stroke-width="2.5" class="mt-0.5 shrink-0 text-slate-400" />
                <span>{{ b }}</span>
              </li>
            </ul>
          </article>
        </div>

        <!-- What-you-get chip row -->
        <div v-reveal class="mt-10 flex flex-wrap items-center justify-center gap-2 text-xs">
          <span
            v-for="chip in chips"
            :key="chip"
            class="rounded-full border border-slate-200 bg-white px-3 py-1 font-medium text-slate-600 shadow-soft"
          >{{ chip }}</span>
        </div>
      </div>
    </section>

    <!-- ============================================================ -->
    <!-- STRATEGY COMPOSER                                             -->
    <!-- ============================================================ -->
    <section id="strategies" class="border-t border-slate-200 bg-slate-50/60">
      <div class="mx-auto max-w-6xl px-6 py-20 lg:py-28">
        <div v-reveal class="mx-auto max-w-3xl text-center">
          <p class="text-xs font-semibold uppercase tracking-[0.18em] text-indigo-600">Strategy Library</p>
          <h2 class="mt-3 text-3xl font-bold tracking-tight text-slate-900 sm:text-4xl">
            Composable, not canned.
          </h2>
          <p class="mt-4 text-base text-slate-600">
            <span class="font-mono text-slate-900">14 entries</span> ×
            <span class="font-mono text-slate-900">6 exits</span> ×
            <span class="font-mono text-slate-900">4 filters</span> — stacked,
            cross-combined, and validated per symbol × timeframe. Every leg is
            independently toggleable and parameter-optimized.
          </p>
        </div>

        <!-- ===== Live Composer Card ===== -->
        <div v-reveal class="mx-auto mt-12 max-w-4xl overflow-hidden rounded-2xl border border-slate-200 bg-white shadow-card">
          <div class="flex items-center justify-between border-b border-slate-200 bg-slate-50/80 px-4 py-2.5">
            <div class="flex items-center gap-2">
              <span class="grid h-5 w-5 place-items-center rounded-md bg-slate-900 text-white">
                <Layers :size="11" :stroke-width="2.25" />
              </span>
              <span class="text-[11px] font-semibold uppercase tracking-wider text-slate-600">Strategy Composer</span>
            </div>
            <div class="flex items-center gap-1.5 font-mono text-[10px] text-slate-500">
              <span class="compile-dot h-1.5 w-1.5 rounded-full bg-indigo-500" />
              <span>compiling · cycle {{ comboIdx + 1 }} / {{ combos.length }}</span>
            </div>
          </div>

          <div class="grid grid-cols-1 gap-px bg-slate-100 md:grid-cols-[1fr_1.1fr]">
            <!-- Left: composer rows -->
            <div class="space-y-px bg-slate-100">
              <div
                v-for="(row, i) in composerRows"
                :key="row.kind"
                class="flex items-center gap-3 bg-white px-5 py-4"
              >
                <div class="flex w-24 shrink-0 items-center gap-2 text-[10px] font-semibold uppercase tracking-wider text-slate-400">
                  <component :is="row.icon" :size="13" :stroke-width="2" class="text-slate-500" />
                  {{ row.kind }}
                </div>
                <div class="relative flex-1">
                  <!-- animated swap value -->
                  <div :key="row.value + comboIdx" class="swap-in flex items-center gap-2">
                    <span :class="['h-1.5 w-1.5 rounded-full', row.dotClass]" />
                    <span class="font-mono text-sm font-semibold text-slate-900">{{ row.value }}</span>
                    <span v-if="row.sub" class="font-mono text-[10px] text-slate-400">{{ row.sub }}</span>
                  </div>
                </div>
                <span class="font-mono text-[11px] text-slate-300">›</span>
              </div>

              <!-- Compiled handle -->
              <div class="bg-slate-900 px-5 py-4 text-white">
                <div class="flex items-center justify-between">
                  <div class="flex items-center gap-2 text-[10px] font-semibold uppercase tracking-wider text-slate-400">
                    <Terminal :size="12" :stroke-width="2" />
                    Compiled
                  </div>
                  <span
                    :class="[
                      'rounded-full px-2 py-0.5 font-mono text-[9px] font-bold tracking-wider',
                      current.verdict === 'STRONG EDGE'
                        ? 'bg-emerald-500/15 text-emerald-300 ring-1 ring-inset ring-emerald-500/30'
                        : 'bg-amber-500/15 text-amber-300 ring-1 ring-inset ring-amber-500/30',
                    ]"
                  >
                    {{ current.verdict }}
                  </span>
                </div>
                <div :key="'handle' + comboIdx" class="swap-in mt-1.5 truncate font-mono text-[12px] text-blue-300">
                  $ sq compile {{ current.handle }}
                </div>
                <div :key="'metrics' + comboIdx" class="swap-in mt-0.5 font-mono text-[10.5px] text-slate-400">
                  {{ current.metrics }}
                </div>
              </div>
            </div>

            <!-- Right: backtest progress + stat tiles -->
            <div class="flex flex-col gap-3 bg-white p-5">
              <div class="flex items-center justify-between text-[10px] font-semibold uppercase tracking-wider text-slate-400">
                <span class="flex items-center gap-1.5">
                  <FlaskConical :size="12" :stroke-width="2" /> Walk-forward validation
                </span>
                <span class="font-mono text-slate-500">train / test</span>
              </div>

              <!-- Segmented progress -->
              <div class="grid grid-cols-12 gap-0.5">
                <span
                  v-for="n in 12"
                  :key="n"
                  class="wf-cell h-5 rounded-[1px]"
                  :class="n <= 8 ? 'bg-indigo-500/80' : 'bg-emerald-500/80'"
                  :style="{ animationDelay: (n * 90) + 'ms' }"
                />
              </div>
              <div class="flex justify-between font-mono text-[10px] text-slate-400">
                <span>train · 8 folds</span><span>test · 4 folds</span>
              </div>

              <!-- Live stat tiles -->
              <div class="mt-2 grid grid-cols-3 gap-2">
                <div class="rounded-lg border border-slate-200 bg-slate-50/70 p-2.5">
                  <div class="text-[9px] font-semibold uppercase tracking-wider text-slate-400">Sharpe</div>
                  <div :key="'sh' + comboIdx" class="swap-in mt-0.5 font-mono text-sm font-bold text-slate-900">{{ current.sharpe }}</div>
                </div>
                <div class="rounded-lg border border-slate-200 bg-slate-50/70 p-2.5">
                  <div class="text-[9px] font-semibold uppercase tracking-wider text-slate-400">p-value</div>
                  <div :key="'p' + comboIdx" class="swap-in mt-0.5 font-mono text-sm font-bold text-slate-900">{{ current.pValue }}</div>
                </div>
                <div class="rounded-lg border border-slate-200 bg-slate-50/70 p-2.5">
                  <div class="text-[9px] font-semibold uppercase tracking-wider text-slate-400">Exp.</div>
                  <div :key="'ex' + comboIdx" class="swap-in mt-0.5 font-mono text-sm font-bold text-emerald-600">{{ current.expectancy }}</div>
                </div>
              </div>

              <div class="mt-auto flex items-center gap-2 rounded-lg border border-slate-200 bg-white p-2.5 text-[10.5px] text-slate-500">
                <ShieldCheck :size="13" :stroke-width="2.25" class="text-emerald-500" />
                <span>Overfit detector filters low-p-value noise before any live deploy.</span>
              </div>
            </div>
          </div>
        </div>

        <!-- ===== Entry / Exit / Filter grids ===== -->
        <div class="mx-auto mt-12 grid max-w-5xl grid-cols-1 gap-6 lg:grid-cols-[1.4fr_1fr]">
          <!-- Entries -->
          <div v-reveal class="rounded-xl border border-slate-200 bg-white p-5 shadow-soft">
            <div class="flex items-center justify-between">
              <h3 class="flex items-center gap-2 text-sm font-semibold text-slate-900">
                <span class="grid h-5 w-5 place-items-center rounded-md bg-emerald-500/10 text-emerald-600">
                  <TrendingUp :size="12" :stroke-width="2.5" />
                </span>
                Entry Signals
              </h3>
              <span class="font-mono text-[10px] text-slate-400">14 primary</span>
            </div>
            <div class="mt-4 grid grid-cols-2 gap-2 sm:grid-cols-3">
              <div
                v-for="(s, i) in entries"
                :key="s"
                :class="[
                  'relative overflow-hidden rounded-lg border px-3 py-2 font-mono text-[10.5px] transition duration-300',
                  s === current.entry
                    ? 'border-emerald-300 bg-emerald-50 text-emerald-700 shadow-soft chip-active'
                    : 'border-slate-200 bg-white text-slate-600 hover:-translate-y-0.5 hover:border-slate-300',
                ]"
                :style="{ transitionDelay: (i * 8) + 'ms' }"
              >
                <div class="flex items-center justify-between">
                  <span class="font-semibold tracking-tight">{{ s }}</span>
                  <span
                    :class="[
                      'h-1.5 w-1.5 rounded-full transition',
                      s === current.entry ? 'bg-emerald-500' : 'bg-slate-300',
                    ]"
                  />
                </div>
              </div>
            </div>
          </div>

          <!-- Exits + Filters -->
          <div class="flex flex-col gap-4">
            <div v-reveal class="rounded-xl border border-slate-200 bg-white p-5 shadow-soft">
              <div class="flex items-center justify-between">
                <h3 class="flex items-center gap-2 text-sm font-semibold text-slate-900">
                  <span class="grid h-5 w-5 place-items-center rounded-md bg-rose-500/10 text-rose-600">
                    <TrendingDown :size="12" :stroke-width="2.5" />
                  </span>
                  Exit Mechanisms
                </h3>
                <span class="font-mono text-[10px] text-slate-400">6 stackable</span>
              </div>
              <div class="mt-4 grid grid-cols-1 gap-2">
                <div
                  v-for="s in exits"
                  :key="s"
                  :class="[
                    'flex items-center justify-between rounded-lg border px-3 py-2 font-mono text-[10.5px] transition duration-300',
                    s === current.exit
                      ? 'border-rose-300 bg-rose-50 text-rose-700 shadow-soft chip-active'
                      : 'border-slate-200 bg-white text-slate-600',
                  ]"
                >
                  <span class="font-semibold tracking-tight">{{ s }}</span>
                  <span
                    :class="[
                      'h-1.5 w-1.5 rounded-full transition',
                      s === current.exit ? 'bg-rose-500' : 'bg-slate-300',
                    ]"
                  />
                </div>
              </div>
            </div>

            <div v-reveal class="rounded-xl border border-slate-200 bg-white p-5 shadow-soft">
              <div class="flex items-center justify-between">
                <h3 class="flex items-center gap-2 text-sm font-semibold text-slate-900">
                  <span class="grid h-5 w-5 place-items-center rounded-md bg-indigo-500/10 text-indigo-600">
                    <Filter :size="12" :stroke-width="2.5" />
                  </span>
                  Filters
                </h3>
                <span class="font-mono text-[10px] text-slate-400">4 composable</span>
              </div>
              <div class="mt-4 flex flex-wrap gap-2">
                <span
                  v-for="s in filters"
                  :key="s"
                  :class="[
                    'rounded-full border px-2.5 py-1 font-mono text-[10.5px] transition duration-300',
                    s === current.filter
                      ? 'border-indigo-300 bg-indigo-50 text-indigo-700 shadow-soft chip-active'
                      : 'border-slate-200 bg-white text-slate-600',
                  ]"
                >{{ s }}</span>
              </div>
            </div>
          </div>
        </div>

        <ul v-reveal class="mx-auto mt-10 grid max-w-3xl grid-cols-1 gap-2 text-sm text-slate-600 sm:grid-cols-3">
          <li class="flex items-center gap-2"><Check :size="14" :stroke-width="2.5" class="text-slate-900" /> Walk-forward train / test</li>
          <li class="flex items-center gap-2"><Check :size="14" :stroke-width="2.5" class="text-slate-900" /> p-value verdict scoring</li>
          <li class="flex items-center gap-2"><Check :size="14" :stroke-width="2.5" class="text-slate-900" /> Per-symbol optimization</li>
        </ul>
      </div>
    </section>

    <!-- ============================================================ -->
    <!-- ARCHITECTURE                                                  -->
    <!-- ============================================================ -->
    <section id="architecture" class="border-t border-slate-200 bg-white">
      <div class="mx-auto max-w-6xl px-6 py-20 lg:py-28">
        <div v-reveal class="mx-auto max-w-2xl text-center">
          <p class="text-xs font-semibold uppercase tracking-[0.18em] text-indigo-600">Architecture</p>
          <h2 class="mt-3 text-3xl font-bold tracking-tight text-slate-900 sm:text-4xl">
            One repo. Every layer. Fully auditable.
          </h2>
          <p class="mt-4 text-base text-slate-600">
            Presentation, API, worker, data — structured for production
            deployment from day one. No black boxes. No vendor lock-in.
          </p>
        </div>

        <!-- IDE window with reveal wipe -->
        <div v-reveal class="mx-auto mt-12 max-w-4xl overflow-hidden rounded-xl border border-slate-200 bg-white shadow-card">
          <div class="flex items-center justify-between border-b border-slate-200 bg-slate-50 px-4 py-2.5">
            <div class="flex items-center gap-1.5">
              <span class="h-3 w-3 rounded-full bg-slate-300" />
              <span class="h-3 w-3 rounded-full bg-slate-300" />
              <span class="h-3 w-3 rounded-full bg-slate-300" />
            </div>
            <div class="flex items-center gap-1.5 rounded-md border border-slate-200 bg-white px-2.5 py-1 text-[11px] font-medium text-slate-500">
              <FileCode2 :size="12" :stroke-width="2" />
              architecture.txt
            </div>
            <div class="flex items-center gap-1.5 font-mono text-[10px] text-slate-400">
              <span class="h-1.5 w-1.5 rounded-full bg-emerald-500" /> compiled
            </div>
          </div>

          <div class="relative">
            <pre class="arch-pre overflow-x-auto px-5 py-6 font-mono text-[11.5px] leading-relaxed text-slate-700 sm:text-xs"><code>┌─────────────────────────────────────────────────────────────────────────┐
│                              PRESENTATION                                │
│  ┌─────────────┐  React 19 + TypeScript + Tailwind CSS + Framer Motion  │
│  │   Next.js   │  Real-time dashboard · Equity, positions, scans        │
│  │   :3000     │  Backtest / regime / audit workspaces                  │
│  └──────┬──────┘                                                         │
├─────────┼───────────────────────────────────────────────────────────────┤
│         │                           API LAYER                            │
│  ┌──────▼──────┐  FastAPI + Pydantic + SQLAlchemy 2.0                   │
│  │   Backend   │  Async/await throughout, automatic OpenAPI docs         │
│  │   :8000     │  JWT auth, rate limiting, request logging               │
│  └──────┬──────┘                                                         │
├─────────┼───────────────────────────────────────────────────────────────┤
│         │                          SERVICES                              │
│  ┌──────▼──────┐  ┌──────────────┐  ┌──────────────┐                     │
│  │   Worker    │  │   Monitor    │  │    Redis     │                     │
│  │ Batch Opt.  │  │ Signal Scan  │  │    Cache     │                     │
│  │ 14 strats   │  │ Live Execute │  │   Pub/Sub    │                     │
│  └──────┬──────┘  └──────┬───────┘  └──────┬───────┘                     │
├─────────┼────────────────┼─────────────────┼────────────────────────────┤
│         │                │                 │                             │
│  ┌──────▼──────┐  ┌──────▼──────┐  ┌───────▼──────┐                      │
│  │ TimescaleDB │  │  Binance    │  │    Email     │                      │
│  │  PostgreSQL │  │ CCXT Futures│  │   Alerts     │                      │
│  └─────────────┘  └─────────────┘  └──────────────┘                      │
└─────────────────────────────────────────────────────────────────────────┘</code></pre>
            <span class="pointer-events-none absolute bottom-6 left-5 inline-block h-3 w-[7px] bg-slate-700 animate-blink" />
          </div>
        </div>

        <div v-reveal class="mx-auto mt-10 grid max-w-4xl grid-cols-2 gap-px overflow-hidden rounded-lg border border-slate-200 bg-slate-200 text-sm sm:grid-cols-4">
          <div v-for="item in stack" :key="item.label" class="flex flex-col gap-0.5 bg-white px-4 py-3">
            <span class="text-[11px] font-semibold uppercase tracking-wider text-slate-400">{{ item.label }}</span>
            <span class="font-medium text-slate-900">{{ item.value }}</span>
          </div>
        </div>
      </div>
    </section>

    <!-- ============================================================ -->
    <!-- PRICING                                                       -->
    <!-- ============================================================ -->
    <section id="pricing" class="border-t border-slate-200 bg-slate-50/60">
      <div class="mx-auto max-w-6xl px-6 py-20 lg:py-28">
        <div v-reveal class="mx-auto max-w-2xl text-center">
          <p class="text-xs font-semibold uppercase tracking-[0.18em] text-indigo-600">Pricing</p>
          <h2 class="mt-3 text-3xl font-bold tracking-tight text-slate-900 sm:text-4xl">
            One-time license. Lifetime source access.
          </h2>
          <p class="mt-4 text-base text-slate-600">
            No subscriptions. No revenue share. No telemetry. Pay once, own the
            codebase.
          </p>
        </div>

        <div class="mx-auto mt-14 grid max-w-4xl grid-cols-1 gap-6 md:grid-cols-2">
          <!-- Sovereign -->
          <div
            v-reveal
            class="group flex flex-col rounded-2xl border border-slate-200 bg-white p-8 shadow-card transition duration-300 hover:-translate-y-1 hover:shadow-xl"
          >
            <div class="flex items-center justify-between">
              <h3 class="text-sm font-semibold uppercase tracking-wider text-slate-500">Sovereign</h3>
              <span class="rounded-full border border-slate-200 bg-slate-50 px-2.5 py-0.5 text-[11px] font-medium text-slate-600">
                Personal Use
              </span>
            </div>
            <div class="mt-5 flex items-baseline gap-1.5">
              <span class="text-5xl font-extrabold tracking-tight text-slate-900">$349</span>
              <span class="text-sm text-slate-500">/ one-time</span>
            </div>
            <p class="mt-3 text-sm text-slate-600">
              For the individual quant operator. Deploy the full system on your
              own infrastructure.
            </p>
            <ul class="mt-8 space-y-3 text-sm text-slate-700">
              <li v-for="f in sovereignFeatures" :key="f" class="flex items-start gap-2.5">
                <Check :size="16" :stroke-width="2.25" class="mt-0.5 shrink-0 text-slate-900" />
                <span>{{ f }}</span>
              </li>
            </ul>
            <a
              href="https://yourstore.lemonsqueezy.com/checkout/buy/sovereign-license"
              class="mt-10 inline-flex items-center justify-center gap-2 rounded-lg border border-slate-300 bg-white px-5 py-3 text-sm font-semibold text-slate-900 transition hover:border-slate-400 hover:bg-slate-50"
            >
              Acquire Sovereign License
              <ArrowRight :size="15" :stroke-width="2.25" class="transition group-hover:translate-x-0.5" />
            </a>
          </div>

          <!-- Enterprise -->
          <div
            v-reveal
            :style="{ '--reveal-delay': '120ms' }"
            class="group relative flex flex-col rounded-2xl border border-slate-900 bg-slate-900 p-8 text-white shadow-card transition duration-300 hover:-translate-y-1 hover:shadow-2xl"
          >
            <div class="pointer-events-none absolute inset-x-8 -top-px h-px bg-gradient-to-r from-transparent via-white/40 to-transparent" aria-hidden="true" />
            <div class="flex items-center justify-between">
              <h3 class="text-sm font-semibold uppercase tracking-wider text-slate-400">Enterprise</h3>
              <span class="rounded-full border border-white/15 bg-white/5 px-2.5 py-0.5 text-[11px] font-medium text-slate-200">
                Commercial / B2B
              </span>
            </div>
            <div class="mt-5 flex items-baseline gap-1.5">
              <span class="text-5xl font-extrabold tracking-tight text-white">$899</span>
              <span class="text-sm text-slate-400">/ one-time</span>
            </div>
            <p class="mt-3 text-sm text-slate-300">
              For funds, prop shops, and teams deploying client-facing or
              revenue-generating systems.
            </p>
            <ul class="mt-8 space-y-3 text-sm text-slate-200">
              <li v-for="f in enterpriseFeatures" :key="f" class="flex items-start gap-2.5">
                <Check :size="16" :stroke-width="2.25" class="mt-0.5 shrink-0 text-white" />
                <span>{{ f }}</span>
              </li>
            </ul>
            <a
              href="https://yourstore.lemonsqueezy.com/checkout/buy/enterprise-license"
              class="mt-10 inline-flex items-center justify-center gap-2 rounded-lg bg-white px-5 py-3 text-sm font-semibold text-slate-900 transition hover:bg-slate-100"
            >
              Acquire Enterprise License
              <ArrowRight :size="15" :stroke-width="2.25" class="transition group-hover:translate-x-0.5" />
            </a>
          </div>
        </div>

        <p class="mx-auto mt-8 max-w-2xl text-center text-xs text-slate-500">
          Secure checkout powered by Lemon Squeezy. Includes VAT where applicable.
          30-day access guarantee — if the private repository is unreachable, you
          get a full refund.
        </p>
      </div>
    </section>

    <!-- ============================================================ -->
    <!-- SUPPORT & CONSTRAINTS                                         -->
    <!-- ============================================================ -->
    <section id="support" class="border-t border-slate-200 bg-white">
      <div class="mx-auto max-w-3xl px-6 py-20 lg:py-24">
        <div v-reveal class="text-center">
          <p class="text-xs font-semibold uppercase tracking-[0.18em] text-indigo-600">Support & Constraints</p>
          <h2 class="mt-3 text-3xl font-bold tracking-tight text-slate-900 sm:text-4xl">
            Designed for self-reliant operators.
          </h2>
          <p class="mt-4 text-sm text-slate-500">
            SovereignQuant assumes proficiency in Python, Docker, and standard
            web technologies. Support is intentionally scoped.
          </p>
        </div>

        <div v-reveal class="mt-12 divide-y divide-slate-200 overflow-hidden rounded-xl border border-slate-200 bg-white">
          <div v-for="(item, i) in faqs" :key="item.q" class="group">
            <button
              type="button"
              class="flex w-full items-center justify-between gap-4 px-6 py-5 text-left transition hover:bg-slate-50"
              :aria-expanded="open === i"
              @click="toggle(i)"
            >
              <span class="text-sm font-semibold text-slate-900">{{ item.q }}</span>
              <Plus
                :size="16"
                :stroke-width="2.25"
                class="shrink-0 text-slate-400 transition duration-200"
                :class="open === i ? 'rotate-45 text-slate-900' : ''"
              />
            </button>
            <div v-show="open === i" class="px-6 pb-5 text-sm leading-relaxed text-slate-500">
              {{ item.a }}
            </div>
          </div>
        </div>

        <p v-reveal class="mx-auto mt-10 max-w-2xl text-center text-[11px] leading-relaxed text-slate-400">
          <span class="font-semibold text-slate-500">FINANCIAL DISCLAIMER —</span>
          SovereignQuant is software, not financial advice. Cryptocurrency
          futures trading involves substantial risk of loss. Past performance
          does not guarantee future results. You are solely responsible for
          strategy development, capital allocation, and regulatory compliance.
          Trade responsibly. Protect your capital.
        </p>
      </div>
    </section>

    <!-- ============================================================ -->
    <!-- FOOTER                                                        -->
    <!-- ============================================================ -->
    <footer class="border-t border-slate-200 bg-slate-50/60">
      <div class="mx-auto flex max-w-6xl flex-col items-center justify-between gap-4 px-6 py-10 text-xs text-slate-500 sm:flex-row">
        <div class="flex items-center gap-2">
          <span class="grid h-5 w-5 place-items-center rounded-md bg-slate-900 text-white">
            <Hexagon :size="12" :stroke-width="2.25" />
          </span>
          <span class="font-medium text-slate-700">SovereignQuant</span>
          <span>© {{ year }}</span>
        </div>
        <div class="flex items-center gap-6">
          <a href="mailto:peeraphol.ka@gmail.com" class="transition hover:text-slate-900">Contact</a>
          <a href="#pricing" class="transition hover:text-slate-900">License</a>
          <a href="#support" class="transition hover:text-slate-900">Disclaimer</a>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup lang="ts">
import {
  Activity,
  ArrowRight,
  ArrowUpRight,
  ArrowDownRight,
  BarChart3,
  Check,
  Crosshair,
  Dices,
  FileCode2,
  Filter,
  FlaskConical,
  Hexagon,
  Layers,
  LayoutDashboard,
  Lock,
  Plus,
  Radar,
  Settings,
  ShieldCheck,
  Target,
  Terminal,
  TrendingDown,
  TrendingUp,
  Wallet,
} from 'lucide-vue-next'
import { computed, onBeforeUnmount, onMounted, ref, type Directive } from 'vue'

const year = computed(() => new Date().getFullYear())

// ---------- Scroll-reveal directive ----------
const vReveal: Directive<HTMLElement> = {
  mounted(el) {
    el.classList.add('reveal')
    const io = new IntersectionObserver(
      (entries) => {
        entries.forEach((e) => {
          if (e.isIntersecting) {
            el.classList.add('reveal-in')
            io.unobserve(el)
          }
        })
      },
      { threshold: 0.12, rootMargin: '0px 0px -40px 0px' }
    )
    io.observe(el)
  },
}

// ---------- Dashboard mock data ----------
const sidebar = [
  { icon: LayoutDashboard, label: 'Dashboard', active: true },
  { icon: Activity,        label: 'Live Trading', active: false },
  { icon: FlaskConical,    label: 'Backtest', active: false },
  { icon: Radar,           label: 'Regime Analytics', active: false },
  { icon: BarChart3,       label: 'Portfolio', active: false },
  { icon: FileCode2,       label: 'Audit', active: false },
  { icon: Settings,        label: 'Settings', active: false },
]

const kpis = [
  { label: 'Total Net PnL',    value: '$12,847.20', delta: '+12.5%', up: true,  icon: Wallet,    tick: 'tick-up' },
  { label: 'Win Rate',         value: '64.3%',      delta: '+5.2%',  up: true,  icon: Target,    tick: 'tick-neutral' },
  { label: 'Active Positions', value: '3',          delta: '',       up: true,  icon: Crosshair, tick: 'tick-neutral' },
  { label: 'Total Trades',     value: '847',        delta: '',       up: true,  icon: Activity,  tick: 'tick-neutral' },
]

const trades = [
  { side: 'LONG',  symbol: 'BTCUSDT',  lev: 10, time: '14:32:08', price: '67,842.50', pnl: '+$284.12', pnlUp: true  },
  { side: 'SHORT', symbol: 'ETHUSDT',  lev: 5,  time: '14:18:42', price: '3,421.80',  pnl: '-$42.60',  pnlUp: false },
  { side: 'LONG',  symbol: 'SOLUSDT',  lev: 20, time: '13:55:11', price: '186.24',    pnl: '',         pnlUp: true  },
  { side: 'LONG',  symbol: 'AVAXUSDT', lev: 10, time: '13:41:08', price: '38.92',     pnl: '+$128.40', pnlUp: true  },
]

// Smooth upward-drifting equity curve
const equityPath =
  'M 0,155 C 30,150 50,148 80,142 C 110,136 130,140 160,128 ' +
  'C 190,116 210,122 240,110 C 270,98 290,102 320,88 ' +
  'C 350,74 370,82 400,68 C 430,54 450,62 480,48 ' +
  'C 510,34 530,40 560,28 C 580,22 590,22 600,24'

const equityArea = equityPath + ' L 600,200 L 0,200 Z'

// ---------- Capabilities / features ----------
const capabilities = [
  {
    icon: FlaskConical,
    title: 'Batch Backtest & Optimization',
    description:
      'Run 14 strategies across hundreds of symbols and timeframes. Automatic overfit filtering with train / test split validation.',
    bullets: [
      '14 built-in strategies, CCXT-compatible',
      'Walk-forward splits with p-value scoring',
      'Per-symbol × per-timeframe parameter search',
    ],
  },
  {
    icon: Dices,
    title: 'Monte Carlo & Risk Controller',
    description:
      '10,000+ stochastic simulations per strategy. Kill switches, portfolio heat, and pre-trade checks on every order.',
    bullets: [
      'VaR / CVaR & drawdown distributions',
      'Position sizer with correlation limits',
      'Kill switch · configurable DD threshold',
    ],
  },
  {
    icon: Radar,
    title: 'Regime-Aware Live Execution',
    description:
      'Uptrend, downtrend, and sideways regimes detected per symbol. Live watchlists gated by allowed regimes.',
    bullets: [
      'Regime detector v2 · ADX + volatility',
      'Allowed-regime filter per watch',
      'Signal monitor · 5m heartbeat',
    ],
  },
]

const chips = [
  'Monitoring Dashboard',
  'Equity Curve',
  'Strategy Health Verdict',
  'Trade Audit Trail',
  'Email Alerts',
  'Docker Compose',
  'JWT Auth',
  'OpenAPI Docs',
  'Encrypted API Keys',
]

// ---------- Strategy Composer ----------
const entries = [
  'MA_CROSSOVER',
  'MA_RSI',
  'RSI_MEAN_REVERSION',
  'MACD',
  'CONNORS_RSI',
  'BB_REVERSION',
  'ENGULFING',
  'HAMMER',
  'DOJI',
  'SUPERTREND',
  'DONCHIAN',
  'VWAP_REVERSION',
  'KELTNER_REVERSION',
  'STOCHRSI_REVERSION',
]

const exits = [
  'SIGNAL_REVERSAL',
  'BB_UPPER_EXIT',
  'FIXED_STOP_LOSS',
  'FIXED_TAKE_PROFIT',
  'TRAILING_STOP',
  'ATR_TRAILING',
]

const filters = [
  'RSI_THRESHOLD',
  'BB_CONFIRMATION',
  'ADX > 25',
  'REGIME · UPTREND',
  'REGIME · DOWNTREND',
  'REGIME · SIDEWAYS',
]

type Combo = {
  entry: string
  exit: string
  filter: string
  handle: string
  sharpe: string
  pValue: string
  expectancy: string
  verdict: 'STRONG EDGE' | 'MARGINAL'
  metrics: string
}

const combos: Combo[] = [
  {
    entry: 'SUPERTREND',
    exit: 'ATR_TRAILING',
    filter: 'REGIME · UPTREND',
    handle: 'supertrend_atr_trail_trend_up --atr=14 --mult=2.5',
    sharpe: '2.18', pValue: '0.01', expectancy: '+0.48R',
    verdict: 'STRONG EDGE',
    metrics: '412 trades · win 62.4% · max DD -8.1%',
  },
  {
    entry: 'MA_CROSSOVER',
    exit: 'SIGNAL_REVERSAL',
    filter: 'ADX > 25',
    handle: 'ma_cross_signal_exit_adx --fast=20 --slow=50',
    sharpe: '1.42', pValue: '0.03', expectancy: '+0.32R',
    verdict: 'STRONG EDGE',
    metrics: '287 trades · win 54.7% · max DD -11.2%',
  },
  {
    entry: 'BB_REVERSION',
    exit: 'BB_UPPER_EXIT',
    filter: 'RSI_THRESHOLD',
    handle: 'bb_reversion_bb_upper_rsi --std=2.0 --rsi=30',
    sharpe: '1.08', pValue: '0.08', expectancy: '+0.21R',
    verdict: 'MARGINAL',
    metrics: '198 trades · win 58.1% · max DD -13.5%',
  },
  {
    entry: 'CONNORS_RSI',
    exit: 'FIXED_TAKE_PROFIT',
    filter: 'REGIME · SIDEWAYS',
    handle: 'connors_rsi_tp_sideways --tp=4% --lookback=3',
    sharpe: '1.74', pValue: '0.02', expectancy: '+0.38R',
    verdict: 'STRONG EDGE',
    metrics: '356 trades · win 67.9% · max DD -7.8%',
  },
  {
    entry: 'MACD',
    exit: 'TRAILING_STOP',
    filter: 'BB_CONFIRMATION',
    handle: 'macd_trail_bbconf --fast=12 --slow=26 --trail=2%',
    sharpe: '1.56', pValue: '0.04', expectancy: '+0.29R',
    verdict: 'STRONG EDGE',
    metrics: '241 trades · win 51.4% · max DD -9.6%',
  },
  {
    entry: 'DONCHIAN',
    exit: 'ATR_TRAILING',
    filter: 'REGIME · UPTREND',
    handle: 'donchian_atr_trail_trend_up --N=20 --mult=3.0',
    sharpe: '1.92', pValue: '0.02', expectancy: '+0.41R',
    verdict: 'STRONG EDGE',
    metrics: '172 trades · win 48.2% · max DD -10.3%',
  },
  {
    entry: 'VWAP_REVERSION',
    exit: 'SIGNAL_REVERSAL',
    filter: 'REGIME · DOWNTREND',
    handle: 'vwap_reversion_signal_down --window=30',
    sharpe: '1.34', pValue: '0.05', expectancy: '+0.26R',
    verdict: 'STRONG EDGE',
    metrics: '224 trades · win 56.8% · max DD -12.1%',
  },
  {
    entry: 'STOCHRSI_REVERSION',
    exit: 'FIXED_STOP_LOSS',
    filter: 'RSI_THRESHOLD',
    handle: 'stochrsi_sl_rsi --k=3 --d=3 --sl=2%',
    sharpe: '0.98', pValue: '0.12', expectancy: '+0.14R',
    verdict: 'MARGINAL',
    metrics: '312 trades · win 63.5% · max DD -15.4%',
  },
]

const comboIdx = ref(0)
const current = computed(() => combos[comboIdx.value])

const composerRows = computed(() => [
  { kind: 'Entry',  icon: TrendingUp,   value: current.value.entry,  sub: '× ',  dotClass: 'bg-emerald-500' },
  { kind: 'Exit',   icon: TrendingDown, value: current.value.exit,   sub: '× ',  dotClass: 'bg-rose-500' },
  { kind: 'Filter', icon: Filter,       value: current.value.filter, sub: '',     dotClass: 'bg-indigo-500' },
])

let cycleTimer: ReturnType<typeof setInterval> | null = null
onMounted(() => {
  cycleTimer = setInterval(() => {
    comboIdx.value = (comboIdx.value + 1) % combos.length
  }, 2200)
})
onBeforeUnmount(() => {
  if (cycleTimer) clearInterval(cycleTimer)
})

const stack = [
  { label: 'Frontend', value: 'Next.js 15 · React 19' },
  { label: 'Backend', value: 'FastAPI · Pydantic v2' },
  { label: 'Database', value: 'TimescaleDB · Redis' },
  { label: 'Deploy', value: 'Docker · Nginx' },
]

const sovereignFeatures = [
  'Full private repository access',
  'Complete source code (backend + frontend + worker)',
  '14 strategies · Monte Carlo · regime detection',
  'Docker Compose deployment stack',
  'Personal, single-operator use',
  'Lifetime core updates',
]

const enterpriseFeatures = [
  'Everything in Sovereign',
  'Commercial / B2B deployment rights',
  'Internal team & client-facing use',
  'Prop-shop & fund usage permitted',
  'Up to 5 internal seats',
  'Priority async issue triage',
]

const faqs = [
  {
    q: 'Does this trade for me automatically?',
    a: 'SovereignQuant is infrastructure, not a signal service. You configure strategies, run the optimization worker, and enable the live monitor. Every trade is triggered by your own validated strategy — there are no proprietary signals from us.',
  },
  {
    q: 'What support is included?',
    a: 'Asynchronous infrastructure support via GitHub Issues and Discussions. Bug reports and access issues are handled transparently in the repository. Expect responses within 48–72 hours on business days.',
  },
  {
    q: 'What is explicitly out of scope?',
    a: 'No strategy consulting, no trading logic advice, no coding tutoring, no 1-on-1 onboarding calls, no custom server deployments. SovereignQuant is an infrastructure product for capable developers.',
  },
  {
    q: 'Can I modify and redistribute the code?',
    a: 'You may modify the code freely for your own deployments under either license. Redistribution, resale, or publishing the source (in whole or in substantial part) is prohibited. See LICENSE for full terms.',
  },
]

const open = ref<number | null>(0)
function toggle(i: number) {
  open.value = open.value === i ? null : i
}
</script>

<style>
html,
body,
#__nuxt {
  background-color: #ffffff;
}

/* =========================================================================
   Entry animations (hero staggered)
   ========================================================================= */
@keyframes fadeUp {
  0%   { opacity: 0; transform: translateY(18px); filter: blur(4px); }
  100% { opacity: 1; transform: translateY(0);    filter: blur(0); }
}
.anim-fade-up {
  opacity: 0;
  animation: fadeUp 0.9s cubic-bezier(0.22, 1, 0.36, 1) forwards;
}
.anim-d-0 { animation-delay: 0.05s; }
.anim-d-1 { animation-delay: 0.15s; }
.anim-d-2 { animation-delay: 0.28s; }
.anim-d-3 { animation-delay: 0.42s; }
.anim-d-4 { animation-delay: 0.55s; }
.anim-d-5 { animation-delay: 0.75s; }

/* =========================================================================
   Scroll-reveal
   ========================================================================= */
.reveal {
  opacity: 0;
  transform: translateY(16px);
  transition:
    opacity 0.8s cubic-bezier(0.22, 1, 0.36, 1),
    transform 0.8s cubic-bezier(0.22, 1, 0.36, 1);
  transition-delay: var(--reveal-delay, 0ms);
  will-change: opacity, transform;
}
.reveal-in {
  opacity: 1;
  transform: translateY(0);
}

/* =========================================================================
   KPI number subtle pulse (tick animations)
   ========================================================================= */
@keyframes tickUp {
  0%, 100% { color: #ffffff; text-shadow: 0 0 0 rgba(16, 185, 129, 0); }
  40%      { color: #d1fae5; text-shadow: 0 0 14px rgba(16, 185, 129, 0.35); }
  70%      { color: #ffffff; }
}
@keyframes tickNeutral {
  0%, 100% { opacity: 1; }
  50%      { opacity: 0.78; }
}
.tick-up      { animation: tickUp 3.2s ease-in-out infinite; }
.tick-neutral { animation: tickNeutral 2.6s ease-in-out infinite; }

/* =========================================================================
   Equity curve draw-in + breathing
   ========================================================================= */
@keyframes drawLine {
  0%   { stroke-dashoffset: 900; }
  100% { stroke-dashoffset: 0; }
}
@keyframes fadeIn {
  0%   { opacity: 0; }
  100% { opacity: 1; }
}
@keyframes dotFloat {
  0%, 100% { transform: translateY(0); }
  50%      { transform: translateY(-3px); }
}
.equity-line {
  stroke-dasharray: 900;
  stroke-dashoffset: 900;
  animation: drawLine 2.2s cubic-bezier(0.22, 1, 0.36, 1) 0.6s forwards;
  filter: drop-shadow(0 4px 10px rgba(59, 130, 246, 0.35));
}
.equity-area {
  opacity: 0;
  animation: fadeIn 1s ease-out 2.2s forwards;
}
.equity-dot {
  opacity: 0;
  animation: fadeIn 0.6s ease-out 2.6s forwards, dotFloat 3s ease-in-out 2.6s infinite;
}

/* =========================================================================
   Recent Execution row slide-in
   ========================================================================= */
@keyframes feedSlide {
  0%   { opacity: 0; transform: translateX(8px); }
  100% { opacity: 1; transform: translateX(0); }
}
.feed-row {
  opacity: 0;
  animation: feedSlide 0.7s cubic-bezier(0.22, 1, 0.36, 1) forwards;
}

/* =========================================================================
   Typing caret
   ========================================================================= */
@keyframes blink {
  0%, 49%   { opacity: 1; }
  50%, 100% { opacity: 0; }
}
.animate-blink { animation: blink 1s steps(1) infinite; }

/* =========================================================================
   Strategy Composer — swap-in on value change, active chip pulse,
   walk-forward cell fade-in, compile dot breath
   ========================================================================= */
@keyframes swapIn {
  0%   { opacity: 0; transform: translateY(4px); filter: blur(3px); }
  100% { opacity: 1; transform: translateY(0);   filter: blur(0); }
}
.swap-in { animation: swapIn 0.45s cubic-bezier(0.22, 1, 0.36, 1); }

@keyframes chipPulse {
  0%, 100% { box-shadow: 0 0 0 0 rgba(15, 23, 42, 0.08); }
  50%      { box-shadow: 0 0 0 6px rgba(15, 23, 42, 0); }
}
.chip-active { animation: chipPulse 1.6s ease-in-out infinite; }

@keyframes wfCell {
  0%   { opacity: 0.25; transform: scaleY(0.4); }
  60%  { opacity: 1;    transform: scaleY(1); }
  100% { opacity: 0.85; transform: scaleY(1); }
}
.wf-cell {
  transform-origin: bottom;
  opacity: 0.25;
  animation: wfCell 1.4s cubic-bezier(0.22, 1, 0.36, 1) forwards;
}

@keyframes compileDot {
  0%, 100% { box-shadow: 0 0 0 0 rgba(99, 102, 241, 0.6); }
  50%      { box-shadow: 0 0 0 6px rgba(99, 102, 241, 0); }
}
.compile-dot { animation: compileDot 1.5s ease-in-out infinite; }

/* =========================================================================
   Architecture pre — reveal wipe once visible
   ========================================================================= */
.reveal-in .arch-pre {
  animation: archReveal 1.4s cubic-bezier(0.22, 1, 0.36, 1);
}
@keyframes archReveal {
  0%   { clip-path: inset(0 100% 0 0); }
  100% { clip-path: inset(0 0 0 0); }
}

/* =========================================================================
   Reduced motion
   ========================================================================= */
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.001ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.001ms !important;
  }
  .reveal { opacity: 1; transform: none; }
  .equity-line { stroke-dashoffset: 0; }
  .equity-area, .equity-dot, .feed-row { opacity: 1; }
}
</style>
