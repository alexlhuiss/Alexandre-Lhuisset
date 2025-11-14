---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: '6rem'


sections:
  - block: resume-biography-3
    content:
      username: admin
      text: ''
      button:
        text: Full CV
        url: uploads/resume.pdf
      headings:
        about: ''
        education: ''
        interests: ''
    design:
      background:
        image:
          filename: stacked-peaks.svg
      spacing:
        padding: ['0', '80px', '0', '0']
      css: |
        section[data-block="resume-biography-3"] .grid {
          gap: 2.5rem;          /* espace général entre les colonnes/éléments */
        }

        @media (min-width: 1024px) {
          section[data-block="resume-biography-3"] .grid {
            column-gap: 4rem;   /* encore plus d'espace entre gauche/droite sur grand écran */
          }
        }
  - block: markdown
    content:
      title: 'Collaborate'
      subtitle: ''
      text: |-
        Do not hesitate to reach out in order to collaborate
    design:
      columns: '1'
  - block: collection
    id: papers
    content:
      title: Featured Publication
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 1
  - block: collection
    content:
      title: Recent Publications
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation
---
