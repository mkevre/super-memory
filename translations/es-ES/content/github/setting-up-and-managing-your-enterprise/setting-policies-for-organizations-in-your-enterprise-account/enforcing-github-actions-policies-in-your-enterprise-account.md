---
title: Requerir las políticas de Github Actions en tu cuenta empresarial
intro: 'Los propietarios de las empresas pueden habilitar, inhabilitar y limitar las {% data variables.product.prodname_actions %} para una cuenta empresarial.'
product: '{% data reusables.gated-features.enterprise-accounts %}'
redirect_from:
  - /github/setting-up-and-managing-your-enterprise-account/enforcing-github-actions-policies-in-your-enterprise-account
  - /github/setting-up-and-managing-your-enterprise/enforcing-github-actions-policies-in-your-enterprise-account
miniTocMaxHeadingLevel: 4
versions:
  free-pro-team: '*'
topics:
  - Enterprise
---

### Acerca de los permisos de las {% data variables.product.prodname_actions %} para tu cuenta empresarial

Predeterminadamente, {% data variables.product.prodname_actions %} se habilita en todas las organizaciones que pertenezcan a una cuenta empresarial. Puedes elegir inhabilitar {% data variables.product.prodname_actions %} para todas las organizaciones que pertenezcan a una cuenta empresarial, o permitirlas únicamente para una organización epecífica. También puedes limitar el uso de acciones públicas, para que las personas solo puedan utilizar acciones locales que existen en tu organización.

Para obtener más información acerca de {% data variables.product.prodname_actions %}, consulta la sección "[Acerca de {% data variables.product.prodname_actions %}](/actions/getting-started-with-github-actions/about-github-actions)".

### Adminsitrar los permisos de {% data variables.product.prodname_actions %} para tu cuenta empresarial

Puedes inhabilitar todos los flujos de trabajo de una empresa o configurar una política que configure qué acciones pueden utilizarse en una organización.

{% data reusables.actions.actions-use-policy-settings %}

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.policies-tab %}
{% data reusables.enterprise-accounts.actions-tab %}
{% data reusables.actions.enterprise-actions-permissions %}
1. Haz clic en **Save ** (guardar).

### Permitir que se ejecuten acciones específicas

{% data reusables.actions.allow-specific-actions-intro %}

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.policies-tab %}
{% data reusables.enterprise-accounts.actions-tab %}
1. Debajo de **Políticas**, selecciona **Permitir las acciones seleccionadas** y agrega tus acciones requeridas a la lista. ![Agregar acciones a la lista de permitidos](/assets/images/help/organizations/enterprise-actions-policy-allow-list.png)

### Habilitar flujos de trabajo para las bifurcaciones de repositorios privados

{% data reusables.github-actions.private-repository-forks-overview %}

#### Configurar la política de bifurcaciones privadas para tu cuenta empresarial

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.policies-tab %}
{% data reusables.enterprise-accounts.actions-tab %}
{% data reusables.github-actions.private-repository-forks-configure %}

### Cnfigurar los permisos para el `GITHUB_TOKEN` para tu empresa

{% data reusables.github-actions.workflow-permissions-intro %}

Puedes configurar los permisos predeterminados para del `GITHUB_TOKEN` en la configuración de tu empresa, organización o repositorio. Si eliges la opción restringida como lo predeterminado en la configuración de tu empresa, esto previene que puedas elegir más configuraciones permisivas en la configuración de tu organización o repositorio.

{% data reusables.github-actions.workflow-permissions-modifying %}

#### Configurar los permisos predeterminados del `GITHUB_TOKEN`

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.policies-tab %}
{% data reusables.enterprise-accounts.actions-tab %}
1. Debajo de **Permisos del flujo de trabajo**, elige si quieres que el `GITHUB_TOKEN` tenga permisos de lectura y escritura para todos los alcances o solo acceso de lectura para el alcance `contents`. ![Configurar los permisos del GITHUB_TOKEN para esta empresa](/assets/images/help/settings/actions-workflow-permissions-enterprise.png)
1. Da clic en **Guardar** para aplicar la configuración.
