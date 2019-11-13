---
layout: post
title:  "Reflektioner över uppgiften"
categories: blog assignment1
comments: true
---

{% include og.html %}

# What do you think of pre-compiling your CSS?

#### Compare to regular CSS:
Svårt att veta hur man ska göra för att ändra i temat. Jag valde att ändra i minima-temat och där fanns en samling förutbestämda variabler som man kunde ändra, till exempel bakgrundsfärg och textfärg. Men jag förstod inte direkt hur man ska göra för att ändra till exempel endast bakgrundsfärgen för "mittkolumnen" (där texten finns).

#### Which techniques did you use?
Jag gick enligt uppgiftsbeskrivningen och använde Jekyll med medföljande css-tema (minima) som jag ändrade i för att uppnå en egen prägel på webbplatsen.

#### Pros and cons?
Fördelen är väl att det går relativt enkelt att få upp en webbsida som ser bra ut direkt, i stället för att behöva göra allt från grunden. Men detta kräver ju att man behärskar alla tekniker och verktyg för det, vilket jag ju inte gör, och därför upplevde jag det som lite bökigt och svårtillgängligt.

# What do you think of static site generators?

De är gjorda för att förenkla skapandet av webbsidor genom att skaparen inte behöver koda allt som ska finnas på sidan/sidorna helt för hand och från grunden. Detta ser jag definitivt fördelen med när man behöver skapa webbsidor snabbt och kanske lite mer "på löpande band". När man dessutom har lärt sig något eller några särskilda SSG:er (till exempel Jekyll) på ett mer djupgående plan, så blir man ju vassare på att göra om webbsidorna till att passa just det man är ute efter just då.

#### What type of projects are they suitable for?

Eftersom webbsidor skapade med SSG:er är statiska är de inte lämpliga för projekt där det krävs någon form av databaskoppling med till exempel användarinloggning eller ifyllnad av data på sidan (formulär). Att använda Disqus, en extern tjänst, är ett sätt att tillåta kommentarer på sidan utan att dessa lagras någonstans i själva webbplatsen. Rent informativa webbplatser är lämpliga för att skapas med en SSG.

# What is robots.txt and how have you configure it for your site?

robots.txt är en textfil i webbplatsens root som innehåller instruktioner för hur sökmotorer ska behandla sidan (och dess undersidor). Sökmotorer använder sig av sökrobotar som söker igenom tillgängligt innehåll på nätet för att samla information. En robots.txt-fil kan instruera sökroboten att söka igenom hela webbplatsen, delar av den, eller inte alls. Jag har valt att inte tillåta sökrobotar på min sida alls.

# What is humans.txt and how have you configure it for your site?

humans.txt kom till som en motsvarighet till robots.txt, för att ge utvecklare möjlighet att "signera" sina webbsidor på ett sätt som inte behövde synas på den synliga webbplatsen. I humans.txt kan man inkludera till exempel namnet på utvecklaren, kontaktuppgifter, dedikationer, information om verktyg som använts, med mera. Jag har valt att inkludera mitt namn, linkedinprofil, och min plats.

# How did you implements comments to blog posts?

Som rekommenderades i uppgiftsbeskrivningen har jag använt Disqus. Jag har införlivat Disqus-kommentarsfält på mina blogposter med hjälp av den guide som Disqus tillhandhåller.

# What is Open Graph and how do you make use of it?

Open Graph är ett verktyg för att inkludera information vid delning av länkar till webbsidor i sociala medier, till exempel Facebook. Genom att inkludera en extra html-fil (via _include) på alla sidor kan man se en liten "blurb" med titel, url, typ, samt bild (i förekommande fall).


{% if page.comments %}

<div id="disqus_thread"></div>
<script>

/**
*  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
*  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables*/
/*
var disqus_config = function () {
this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
};
*/
(function() { // DON'T EDIT BELOW THIS LINE
var d = document, s = d.createElement('script');
s.src = 'https://1dv022-sp222xw.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>

{% endif %} 
