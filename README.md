import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { PlayIcon, BookOpen, Gamepad2, Users, Mail } from "lucide-react";

const resources = [
  {
    title: "Livres sur le harcèlement",
    icon: <BookOpen className="w-8 h-8 text-blue-600" />,
    description: "Sélection de romans, BD et essais adaptés aux collégiens, lycéens et étudiants.",
    link: "#livres",
  },
  {
    title: "Jeux vidéo éducatifs",
    icon: <Gamepad2 className="w-8 h-8 text-green-600" />,
    description: "Des jeux pour apprendre à reconnaître, prévenir et agir contre le harcèlement.",
    link: "#jeux",
  },
  {
    title: "Vidéos et témoignages",
    icon: <PlayIcon className="w-8 h-8 text-red-600" />,
    description: "Documentaires, témoignages d’élèves, conseils d’experts pour ouvrir le dialogue.",
    link: "#videos",
  },
  {
    title: "Ressources pour enseignants et parents",
    icon: <Users className="w-8 h-8 text-purple-600" />,
    description: "Guides pédagogiques, outils de prévention, formations et conseils pratiques pour accompagner les jeunes.",
    link: "#enseignants-parents",
  },
];

export default function SensibilisationHarcèlement() {
  return (
    <div className="p-6 max-w-6xl mx-auto">
      <header className="text-center mb-10">
        <h1 className="text-4xl font-bold mb-2">Stop Harcèlement</h1>
        <p className="text-lg text-gray-700">
          Un espace ressource pour lutter ensemble contre le harcèlement, de la 6e à l’université.
        </p>
      </header>

      <section className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6 mb-12">
        {resources.map((res, index) => (
          <Card key={index} className="rounded-2xl shadow-md hover:shadow-xl transition">
            <CardContent className="p-6 flex flex-col items-center text-center">
              {res.icon}
              <h2 className="text-xl font-semibold mt-4 mb-2">{res.title}</h2>
              <p className="text-sm text-gray-600 mb-4">{res.description}</p>
              <Button variant="outline" asChild>
                <a href={res.link}>Explorer</a>
              </Button>
            </CardContent>
          </Card>
        ))}
      </section>

      <section id="contact" className="mb-16">
        <div className="bg-gray-100 p-6 rounded-2xl shadow-md">
          <h2 className="text-2xl font-bold mb-4 flex items-center gap-2">
            <Mail className="w-6 h-6 text-blue-500" />
            Partenariats scolaires
          </h2>
          <p className="text-sm text-gray-700 mb-6">
            Vous représentez un établissement ou une structure éducative et souhaitez collaborer avec nous ? Merci de remplir le formulaire ci-dessous.
          </p>
          <div className="w-full aspect-[4/3]">
            <iframe
              src="https://docs.google.com/forms/d/e/TON_LIEN_PERSO/viewform?embedded=true"
              width="100%"
              height="100%"
              frameBorder="0"
              className="w-full h-full rounded-xl"
              allowFullScreen
              title="Formulaire de partenariat"
            >
              Chargement…
            </iframe>
          </div>
        </div>
      </section>

      <footer className="text-center text-sm text-gray-500">
        © 2025 Stop Harcèlement — Créé pour sensibiliser, éduquer et agir.
      </footer>
    </div>
  );
}
import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Gamepad2 } from "lucide-react";

// Composant SensibilisationJeux
export function SensibilisationJeux() {
  const games = [
    {
      title: "Sea of Solitude",
      description:
        "Un jeu où vous incarnez Kay, une jeune femme luttant contre la solitude et l'isolement, une métaphore de la stigmatisation sociale.",
      platform: "PC, PS4, Xbox",
      link: "https://www.ea.com/games/sea-of-solitude",
    },
    {
      title: "Life is Strange (épisode avec Kate Marsh)",
      description:
        "Ce jeu aborde le harcèlement scolaire, les pressions sociales et leurs conséquences, notamment le traumatisme causé par l'intimidation.",
      platform: "PC, PS4, Xbox",
      link: "https://www.lifeisstrange.com/",
    },
    {
      title: "Emily is Away",
      description:
        "Un jeu simulant des conversations sur une messagerie instantanée, qui aborde le cyberharcèlement et la pression sociale en ligne.",
      platform: "PC",
      link: "https://store.steampowered.com/app/398490/Emily_Is_Away/",
    },
    {
      title: "STOP la violence ! (CANOPE)",
      description:
        "Un jeu éducatif pour sensibiliser les collégiens et lycéens aux comportements violents et à la manière d'y faire face.",
      platform: "Web",
      link: "https://www.reseau-canope.fr/stop-la-violence.html",
    },
    {
      title: "Respect Zone Challenge",
      description:
        "Un jeu interactif pour aider les joueurs à reconnaître et réagir face aux discours haineux, cyberharcèlement et autres violences en ligne.",
      platform: "Web",
      link: "https://www.respectzone.org/",
    },
    {
      title: "Vinz et Lou (Cyberharcèlement)",
      description:
        "Jeu pour sensibiliser les jeunes au cyberharcèlement, avec des missions liées aux réseaux sociaux et des conseils pour prévenir l'intimidation.",
      platform: "Web",
      link: "https://www.vinzetlou.com/",
    },
    {
      title: "2025 ExMachina",
      description:
        "Un jeu qui aborde les thèmes des traces numériques et du harcèlement, adapté aux collégiens et lycéens.",
      platform: "Web",
      link: "https://www.exmachina2025.com/",
    },
    {
      title: "Jeu de plateau en ligne sur la gestion des conflits",
      description:
        "Jeu de groupe pour sensibiliser les élèves à la gestion des conflits et aux comportements respectueux, applicable à la classe ou en ligne.",
      platform: "Physique ou adaptabilité en ligne",
      link: "https://www.trictrac.net/",
    },
    {
      title: "Escape game pédagogique sur les réseaux sociaux et le harcèlement",
      description:
        "Un jeu de réflexion pour sensibiliser les jeunes aux dangers du cyberharcèlement à travers des énigmes et des mises en situation.",
      platform: "Adaptable en ligne ou en classe",
      link: "https://www.escapegame-prevention.fr/",
    },
  ];

  return (
    <div className="p-6 max-w-6xl mx-auto">
      <header className="text-center mb-10">
        <h1 className="text-4xl font-bold mb-2">Jeux Vidéo Educatifs contre le Harcèlement</h1>
        <p className="text-lg text-gray-700">
          Découvrez des jeux qui sensibilisent à la prévention du harcèlement scolaire et du cyberharcèlement.
        </p>
      </header>

      <section className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6 mb-12">
        {games.map((game, index) => (
          <Card key={index} className="rounded-2xl shadow-md hover:shadow-xl transition">
            <CardContent className="p-6 flex flex-col items-center text-center">
              <Gamepad2 className="w-8 h-8 text-green-600" />
              <h2 className="text-xl font-semibold mt-4 mb-2">{game.title}</h2>
              <p className="text-sm text-gray-600 mb-4">{game.description}</p>
              <p className="text-sm text-gray-500 mb-4">Plateforme: {game.platform}</p>
              <Button variant="outline" asChild>
                <a href={game.link} target="_blank" rel="noopener noreferrer">
                  Découvrir le jeu
                </a>
              </Button>
            </CardContent>
          </Card>
        ))}
      </section>
    </div>
  );
}
