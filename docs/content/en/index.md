---
seo:
  title: HAER HCM - Modern Human Capital Management
  description: Enterprise-grade Human Capital Management system featuring multi-tenant architecture, effective dating, and comprehensive workforce management. Built with NestJS, Nuxt 4, and PostgreSQL.
---

::u-page-hero
#title
Next-Generation Human Capital Management

#description
Enterprise-grade HCM platform with multi-tenant architecture, effective dating for complete audit trails, and a modern API-first design. :br Manage your entire workforce lifecycle with confidence.

#links
  :::u-button
  ---
  color: neutral
  size: xl
  to: /en/getting-started/introduction
  trailing-icon: i-lucide-arrow-right
  ---
  Get Started
  :::

  :::u-button
  ---
  color: neutral
  icon: i-lucide-book-open
  size: xl
  to: /en/product/organization
  variant: outline
  ---
  Explore Features
  :::

#headline
  :::u-button{size="sm" to="/en/getting-started/quick-start" variant="outline"}
  Quick Start Guide
  :::
::

::u-page-section
  :::u-page-grid
    ::::u-page-card
    ---
    spotlight: true
    class: group col-span-2 lg:col-span-1
    ---
    #title
    [HAER API]{.text-primary} Backend

    #description
    Powerful REST API built with NestJS + Fastify + Prisma. Features complete multi-tenancy, role-based access control, and enterprise-grade security with JWT authentication.
    ::::

    ::::u-page-card
    ---
    spotlight: true
    class: group col-span-2 lg:col-span-1
    ---
    #title
    [HAER Web]{.text-primary} Frontend

    #description
    Modern, responsive dashboard built with Nuxt 4 + Vue 3, shadcn-vue components, and TailwindCSS. Provides intuitive workforce management with beautiful visualizations.
    ::::

    ::::u-page-card
    ---
    spotlight: true
    class: col-span-2
    ---
    #title
    [Flexible]{.text-primary} Architecture

    #description
    Model complex organizational structures with 5 configurable hierarchy levels (L1-L5), 4-tier job architecture (J1-J4), and unlimited custom fields to adapt to any business requirement.
    ::::

    ::::u-page-card
    ---
    spotlight: true
    class: col-span-2 md:col-span-1
    ---
      :::::div{.bg-elevated.rounded-lg.p-4.text-sm.font-mono.overflow-x-auto}
      ```ts
      // Effective Dating (Time-Travel)
      const employee = await service
        .findByCode(
          "EMP001",
          tenantId,
          { asOf: new Date("2024-01-15") }
        );
      // Returns state as of Jan 15, 2024
      ```
      :::::

    #title
    [Effective Dating]{.text-primary} & Audit Trails

    #description
    Complete temporal data management with version history. Query historical states, track all changes, and maintain regulatory compliance.
    ::::

    ::::u-page-card
    ---
    spotlight: true
    class: col-span-2 md:col-span-1
    ---
      :::::div{.bg-elevated.rounded-lg.p-4.text-sm.font-mono.overflow-x-auto}
      ```ts
      // Multi-Tenant Isolation
      @UseGuards(TenantGuard)
      async findAll(
        @TenantId() tenantId: string
      ) {
        return this.service.findAll(tenantId);
      }
      ```
      :::::

    #title
    [Multi-Tenant]{.text-primary} by Design

    #description
    Native multi-tenancy with complete data isolation. Support multiple clients in a single deployment with separate workspaces.
    ::::

    ::::u-page-card
    ---
    spotlight: true
    class: col-span-2
    ---
    #title
    Comprehensive [Product Modules]{.text-primary}

    #description
    Complete workforce management suite: organizational structure, job architecture, employee management, attendance tracking, and leave management.
    ::::

    ::::u-page-card
    ---
    spotlight: true
    class: col-span-2 lg:col-span-1
    ---
    #title
    Modern [Backend Stack]{.text-primary}

    #description
    Built on battle-tested technologies: NestJS + Fastify for high performance, Prisma ORM for type-safe database access, and PostgreSQL for reliability.
    ::::

    ::::u-page-card
    ---
    spotlight: true
    class: col-span-2 lg:col-span-1
    ---
    #title
    Cutting-Edge [Frontend Stack]{.text-primary}

    #description
    Beautiful interface with Nuxt 4 + Vue 3, TailwindCSS v4, shadcn-vue components, dark mode support, and optimized performance with Vite.
    ::::

    ::::u-page-card
    ---
    spotlight: true
    class: col-span-2
    ---
    #title
    [Production-Ready]{.text-primary} from Day One

    #description
    Built for enterprise: JWT authentication, RBAC security, OpenTelemetry observability, and containerized deployment options.
    ::::
  :::
::
