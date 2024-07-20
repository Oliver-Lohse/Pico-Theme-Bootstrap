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
          ...
          ...

## CTA und Geo

Beiträge können zusätzliche CTA (Call to Actions) oder auch Geo-Koordinaten aufnehmen und durch das Theme anzeigen lassen. Der Metabereich der Beiträge wird daher wie folgt aufgebaut:

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