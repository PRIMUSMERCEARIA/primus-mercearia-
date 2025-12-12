# primus-mercearia-
Site para cardápio digital da Mercearia Primus.
<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Primos Mercearia — Mercearia de Bairro | Pedidos via WhatsApp</title>
    <meta name="description" content="Primos Mercearia — produtos frescos, ofertas do dia, entregas rápidas no seu bairro. Faça pedidos pelo WhatsApp." />
    
    <!-- Open Graph / Facebook -->
    <meta property="og:type" content="website" />
    <meta property="og:title" content="Primos Mercearia — Mercearia de Bairro" />
    <meta property="og:description" content="Produtos frescos e entrega rápida. Peça pelo WhatsApp!" />
    <meta property="og:image" content="https://images.unsplash.com/photo-1542838132-92c53300491e?auto=format&fit=crop&w=1200&q=80" />

    <!-- Twitter -->
    <meta name="twitter:card" content="summary_large_image" />

    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Roboto:wght@400;500;700&display=swap" rel="stylesheet">

    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
      tailwind.config = {
        theme: {
          extend: {
            colors: {
              primary: '#2e7d32', // Green
              secondary: '#FFD93D', // Yellow
              accent: '#FF4B4B', // Red
              neutral: '#f3f3f3',
            },
            fontFamily: {
              sans: ['Inter', 'sans-serif'],
              heading: ['Roboto', 'sans-serif'],
            }
          }
        }
      }
    </script>
    
    <!-- JSON-LD LocalBusiness -->
    <script type="application/ld+json">
      {
        "@context": "https://schema.org",
        "@type": "LocalBusiness",
        "name": "Primos Mercearia",
        "image": "https://images.unsplash.com/photo-1542838132-92c53300491e",
        "telephone": "+55SEUNUMERO",
        "address": {
          "@type": "PostalAddress",
          "streetAddress": "Rua Exemplo, 123",
          "addressLocality": "Seu Bairro",
          "addressRegion": "SP",
          "postalCode": "00000-000",
          "addressCountry": "BR"
        },
        "priceRange": "$",
        "openingHoursSpecification": [
          {
            "@type": "OpeningHoursSpecification",
            "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
            "opens": "07:00",
            "closes": "20:00"
          },
          {
            "@type": "OpeningHoursSpecification",
            "dayOfWeek": "Saturday",
            "opens": "07:00",
            "closes": "13:00"
          }
        ]
      }
    </script>
  <script type="importmap">
{
  "imports": {
    "react": "https://esm.sh/react@^19.2.3",
    "react-dom/": "https://esm.sh/react-dom@^19.2.3/",
    "react/": "https://esm.sh/react@^19.2.3/",
    "lucide-react": "https://esm.sh/lucide-react@^0.561.0"
  }
}
</script>
</head>
  <body class="bg-gray-50 text-gray-900 antialiased selection:bg-primary selection:text-white">
    <div id="root"></div>
  </body>
</html>
