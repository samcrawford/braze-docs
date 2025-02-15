---
nav_title: Définir une catégorie de fil d’actualités
article_title: Définir une catégorie de fils d’actualités pour iOS
platform: iOS
page_order: 4
description: "Cet article de référence montre comment définir une catégorie de fil d’actualités dans votre application iOS."
channel:
  - Fil d’actualité

---

# Définir une catégorie de fil d’actualités

Les instances du fil d’actualité Braze peuvent être configurées pour ne recevoir que des cartes d’une catégorie donnée. Cela permet l’intégration efficace de plusieurs flux de fils d’actualité au sein d’une seule application. Pour plus d’informations sur cette fonctionnalité, consultez nos [meilleures pratiques][40] concernant le fil d’actualités

Les catégories de fil d’actualités peuvent être définies en appelant l’une des méthodes suivantes lorsque vous chargez le fil d’actualités :

{% tabs %}
{% tab OBJECTIVE-C %}

```objc
[newsFeed setCategories:ABKCardCategoryAll];
[newsFeed setCategories:ABKCardCategoryAnnouncements];
[newsFeed setCategories:ABKCardCategoryAdvertising];
[newsFeed setCategories:ABKCardCategorySocial];
[newsFeed setCategories:ABKCardCategoryNews];
[newsFeed setCategories:ABKCardCategoryNoCategory];
```

{% endtab %}
{% tab swift %}

```swift
newsFeed.categories = ABKCardCategory.all
newsFeed.categories = ABKCardCategory.announcements
newsFeed.categories = ABKCardCategory.advertising
newsFeed.categories = ABKCardCategory.social
newsFeed.categories = ABKCardCategory.news
newsFeed.categories = ABKCardCategory.noCategory
```

{% endtab %}
{% endtabs %}


Vous pouvez également remplir un flux avec une combinaison de catégories comme dans l’exemple suivant :

{% tabs %}
{% tab OBJECTIVE-C %}

```objc
[newsFeed setCategories:ABKCardCategoryAnnouncements|ABKCardCategoryAdvertising];
```

{% endtab %}
{% tab swift %}

```swift
newsFeed.categories = ABKCardCategory([.announcements, .advertising])
```

{% endtab %}
{% endtabs %}

[40]: {{site.baseurl}}/user_guide/message_building_by_channel/in-app_messages/reporting/
