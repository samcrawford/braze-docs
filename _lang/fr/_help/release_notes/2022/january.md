---
nav_title: Janvier
page_order: 12
noindex: true
page_type: update
description: "Cet article contient les notes de version de janvier 2022."
---
# Janvier 2022

Bienvenue dans une nouvelle année !

## Mise à jour de l’endpoint d’exportation des utilisateurs

À partir de décembre 2021, les modifications suivantes prennent effet pour l’endpoint [export users by segment]({{site.baseurl}}/api/endpoints/export/user_data/post_users_segment/) (exporter les utilisateurs par segment) :

1. Le champ `fields_to_export` sera requis dans cette requête API. L’option « Tous les champs par défaut » sera supprimée.
2. Les champs pour `custom_events`, `purchases`, `campaigns_received` et `canvases_received` contiendront uniquement les données des 90 derniers jours.

## Nouvelles propriétés pour les événements d’engagement sur les messages Currents

De nouvelles propriétés ont été ajoutées à certains[événements d’engagement sur les messages]({{site.baseurl}}/user_guide/data_and_analytics/braze_currents/event_glossary/message_engagement_events/). Cette mise à jour s’applique aux événements d’engagement sur les messages Currents suivants et à tous les partenaires qui les utilisent :

- Ajouter `LINK_ID`, `LINK_ALIAS` à :
  - Clic sur E-mail (toutes les destinations)
- Ajouter `USER_AGENT` à :
  - Ouverture des e-mails
  - Clics sur les e-mails
  - E-mails marqués comme spam
- Ajouter `MACHINE_OPEN` à :
  - Ouverture des e-mails

## Nouveau tag de personnalisation Liquid

Nous prenons désormais en charge le ciblage des utilisateurs qui ont activé les notifications push lorsque l’application est au premier plan, via les tags Liquid suivants :

{% raw %}
- `{{most_recently_used_device.${foreground_push_enabled}}}`
- `{{targeted_device.${foreground_push_enabled}}}`
{% endraw %}

Pour plus d’informations, consultez les [tags de personnalisation prises en charge]({{site.baseurl}}/user_guide/personalization_and_dynamic_content/liquid/supported_personalization_tags/).

## À propos des webhooks

Les webhooks sont des outils puissants et flexibles, mais ils peuvent être un peu déroutants. Si vous demandez à quoi servent les webhooks et comment vous pouvez les utiliser dans Braze, consultez notre nouvel article [À propos des webhooks]({{site.baseurl}}/user_guide/message_building_by_channel/webhooks/understanding_webhooks/).

## Amazon Personalize

Amazon Personalize c’est comme avoir un système personnel de recommandation de machine learning d’Amazon. Avec ses 20 ans et plus d’expérience en recommandation, Amazon Personalize vous permet d’améliorer l’engagement client en mettant en œuvre des recommandations personnalisées en temps réel sur les produits et le contenu et les promotions marketing ciblées. 

Si vous souhaitez en savoir plus, consultez notre nouvel article [Amazon Personalize]({{site.baseurl}}/partners/message_personalization/dynamic_content/amazon_personalize/amazon_personalize/) pour voir les cas d’utilisation possibles, les données qu’il utilise, comment le configurer et comment l’intégrer à Braze.

## Nouveaux partenariats Braze

### Yotpo – eCommerce

Avec l’intégration entre Braze et [Yotpo]({{site.baseurl}}/partners/message_orchestration/channel_extensions/ecommerce/yotpo/), vous pouvez extraire et afficher de façon dynamique les meilleures évaluations, les meilleurs avis et le contenu visuel généré par les utilisateurs sur les produits dans vos e-mails et autres canaux de communication de Braze. Vous pouvez également inclure les données de fidélisation des clients dans les e-mails et autres méthodes de communication pour créer une interaction plus personnalisée, ce qui stimule les ventes et la fidélisation.

### Zeotap – Plateforme de données client

Avec l’intégration entre Braze et [Zeotap]({{site.baseurl}}/partners/data_and_infrastructure_agility/customer_data_platform/zeotap/), vous pouvez étendre l’ampleur et la portée de vos campagnes en synchronisant et en mappant les données utilisateur Zeotap vers les comptes utilisateur Braze. Vous pouvez ensuite vous servir de ces données pour offrir des expériences personnalisées et ciblées à vos utilisateurs.