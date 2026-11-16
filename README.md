# Schema Templates for Local and Trade Businesses

Copy-paste JSON-LD for plumbers, electricians, HVAC firms, law firms and recruiters. Replace every value in capitals with your real details, then test the result before publishing.

Maintained by [Farman Rind](https://farmanrind.com). Last checked: 16 November 2026. Types and properties come from [schema.org](https://schema.org). Google's structured data rules change, so confirm against the [Rich Results Test](https://search.google.com/test/rich-results).

## Rules before you paste

1. Only mark up what is visible on the page. If the page does not show the phone number, hours or reviews, do not put them in the schema.
2. Use one LocalBusiness block per location page. Do not copy the same block across every page.
3. Keep name, address and phone identical to your Google Business Profile.
4. Never mark up reviews you wrote yourself or reviews you cannot show on the page.
5. Test every template in the Rich Results Test and the Schema Markup Validator before going live.

## Template 1: Plumber

Swap `Plumber` for `Electrician`, `HVACBusiness`, `Locksmith` or `RoofingContractor` to cover other trades. All are LocalBusiness subtypes on schema.org.

```json
{
  "@context": "https://schema.org",
  "@type": "Plumber",
  "@id": "https://WWW.YOURSITE.COM/#business",
  "name": "BUSINESS NAME",
  "url": "https://WWW.YOURSITE.COM/",
  "logo": "https://WWW.YOURSITE.COM/logo.png",
  "image": "https://WWW.YOURSITE.COM/team-photo.jpg",
  "telephone": "+00-0000-000-000",
  "email": "hello@YOURSITE.COM",
  "priceRange": "$$",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "STREET ADDRESS",
    "addressLocality": "CITY",
    "addressRegion": "STATE OR REGION",
    "postalCode": "POSTCODE",
    "addressCountry": "COUNTRY CODE"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 0.0,
    "longitude": 0.0
  },
  "areaServed": [
    { "@type": "City", "name": "CITY ONE" },
    { "@type": "City", "name": "CITY TWO" }
  ],
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
      "opens": "07:00",
      "closes": "17:00"
    }
  ],
  "sameAs": [
    "https://www.google.com/maps?cid=YOUR_CID",
    "https://www.facebook.com/YOURPAGE",
    "https://www.linkedin.com/company/YOURCOMPANY"
  ],
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Services",
    "itemListElement": [
      { "@type": "Offer", "itemOffered": { "@type": "Service", "name": "Blocked drain repair" } },
      { "@type": "Offer", "itemOffered": { "@type": "Service", "name": "Hot water system installation" } }
    ]
  }
}
```

## Template 2: Law firm

Use `LegalService` for a firm, or `Attorney` for a single practitioner.

```json
{
  "@context": "https://schema.org",
  "@type": "LegalService",
  "@id": "https://WWW.YOURSITE.COM/#firm",
  "name": "FIRM NAME",
  "url": "https://WWW.YOURSITE.COM/",
  "logo": "https://WWW.YOURSITE.COM/logo.png",
  "telephone": "+00-0000-000-000",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "STREET ADDRESS",
    "addressLocality": "CITY",
    "postalCode": "POSTCODE",
    "addressCountry": "COUNTRY CODE"
  },
  "areaServed": { "@type": "Country", "name": "COUNTRY" },
  "knowsAbout": ["PRACTICE AREA ONE", "PRACTICE AREA TWO"],
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
      "opens": "09:00",
      "closes": "17:00"
    }
  ],
  "sameAs": ["https://www.linkedin.com/company/YOURFIRM"]
}
```

## Template 3: Recruitment agency

Use `EmploymentAgency`.

```json
{
  "@context": "https://schema.org",
  "@type": "EmploymentAgency",
  "@id": "https://WWW.YOURSITE.COM/#agency",
  "name": "AGENCY NAME",
  "url": "https://WWW.YOURSITE.COM/",
  "logo": "https://WWW.YOURSITE.COM/logo.png",
  "telephone": "+00-0000-000-000",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "STREET ADDRESS",
    "addressLocality": "CITY",
    "postalCode": "POSTCODE",
    "addressCountry": "COUNTRY CODE"
  },
  "areaServed": { "@type": "Country", "name": "COUNTRY" },
  "knowsAbout": ["INDUSTRY ONE", "INDUSTRY TWO"],
  "sameAs": ["https://www.linkedin.com/company/YOURAGENCY"]
}
```

## Add an FAQ block (only if the FAQs are visible on the page)

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "QUESTION EXACTLY AS SHOWN ON THE PAGE",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "ANSWER EXACTLY AS SHOWN ON THE PAGE"
      }
    }
  ]
}
```

Google has limited FAQ rich results to a small set of sites, so do not expect an FAQ snippet. The markup can still describe the page content clearly to machines.

## Where to put it

- WordPress: a header/footer snippet plugin, or your SEO plugin's custom schema field. Wrap the JSON in `<script type="application/ld+json">` and `</script>`.
- Webflow: page settings, Custom Code, Inside head tag.
- Any site: paste the script tag into the `<head>` of the page.

## Check it

1. Rich Results Test: confirm there are no errors.
2. Schema Markup Validator (validator.schema.org): confirm the types and properties are recognised.
3. Compare every value with the visible page and your Google Business Profile.

## Use it

Free to use and share with credit. Spotted a wrong property or a missing trade type? Open an issue and I will fix it.
