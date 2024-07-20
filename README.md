# Pico-Theme-Bootstrap

Dieses Theme basiert auf dem CSS-Framework **Bootstrap** und bildet eine grundlegende Basis für weitere Entwicklungen. Das Theme versucht alle implementierten Funktionen im Template auch sichtbar zu gestalten.

## Affiliates

Das Theme zeigt Affiliates in Kategorien und Beiträgen an. Affiliates werden in der Datei `pico-theme.yml` abgelegt, etwa so:

    affiliate:
        - cta: 
          title:       Titel des Produktes
          description: kurze Beschreibung des Affiliate-Links
          logo:        Link zu einer Bildsource
          url:
      
        - cta:
          title:       ...
          ...

Sie können beliebig viele Affiliates in der `pico-theme.yml` ablegen, die dann zufällig auf der Webseite eingeblendet werden.

## CTA und Geo-Position

Beiträge können zusätzliche CTA (Call to Actions) oder auch Geo-Koordinaten aufnehmen und durch das Theme anzeigen lassen. CTA-Links sind beispielsweise für Downloads sehr gut geeignet, während Geo-Verweise Locationen für Veranstaltungen und ähnliches anzeigen können.

Der Metabereich der Beiträge wird daher wie folgt aufgebaut:

    ---
    Title:              Beitragstitel...
    Author:             Oliver Lohse
    Date:               2024-07-20
    Robots:             all
    Template:           post
    Tags:               Breadcrumb,Navigation,PicoPagesList
    Sticky:             true
    Geo:
        Title:          Standort auf Karte ansehen
        Link:           https://maps.app.goo.gl/G1VBCx5KYBX5rUda8
        Description:    Standort
    CTA:
        Title:          Download
        Link:           https://github.com/Oliver-Lohse/PICO-Twig-Modul-PagesList
        Description:    Laden Sie das fertige Twig-Modul aus diesem Beitrag ganz bequem von GitHub herunter
    Logo:               logo-blue.svg
    Description:        Beschreibung des Beitrags, max 160 Char...
    ---
    ...Beitragstext... ... ...
    ...

>In den meisten Fällen können die Attribute CTA und Geo weggelassen und erst bei Bedarf hinzugefügt werden.

## Sticky - Beitrag nach oben schieben

Beiträge können auf der Startseite nach oben geschoben werden, sofern diese mit dem Status `Sticky: true` versehen sind.

## Sticky - weights

Beiträge die mit `Sticky: true` auf die Startseite geschoben werden, können unterschiedlich breit sein, je nach Beitragsbild kann die Gewichtung von 1 bis 12 in der `pico-theme.yml` individuell eingestellt werden. Selbes kann auch für **Kategorien** vorgegeben werden.

## Plugins

Das Theme nutzt das Plugin `TableOfContents`