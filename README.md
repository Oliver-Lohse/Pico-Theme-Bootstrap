# Pico-Theme-Bootstrap

Dieses Theme basiert auf dem CSS-Framework **Bootstrap** und bildet eine grundlegende Basis für weitere Entwicklungen. Das Theme versucht alle implementierten Funktionen im Template auch sichtbar zu gestalten und soll damit eine Maximalausprägung demonstrieren, wie beispielsweise:

- zufällige Affiliate-Links
- CTA in Beiträgen für Downloads oder sonstige Links
- Geo-Position für Localisierung von Events oder Orten
- individuelle Teaser-Breiten für hervorgehobene Beiträge
- Beiträge können auf die Startseite verschoben werden
- Beiträge und Kategorien können unendlich tief geschachtelt werden
- verwandte Beiträge werden über Schlagwort-Beziehungen angezeigt
- im Beitrag können weitere Beiträge des aktuellen Ordners angezeigt werden
- Social-Bar für Instagram, GitHub, YouTube, Facebook, uvam.
- abonierbarer RSS-Feed
- 404 Error-Page
- global_author statt einen dedizierten Autor im Text

>Die Maximalausprägung kann bei Bedarf schrittweise reduziert werden, indem einige Funktionen deaktiviert werden.

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

## Social Bar

Das Theme blendet eine Social-Bar mit Icons für:

- Instagram
- YouTube
- Twitter
- Xing
- Twitter
- RSS-Feed
- Mail
- GitHub

im unteren Bereich ein.

## Plugins

Das Theme nutzt das Plugin `TableOfContents`

## Installation

Kopieren Sie das Verzeichnis nach dem Download oder Clone in das Verzeichnis: `pico/theme` und passen den Parameter `theme: Pico-Theme-Bootstrap` in der `config.yml` entsprechend an, damit Pico das neue Theme starten kann.