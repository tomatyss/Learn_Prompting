---
sidebar_position: 97
---

# 🟢 OpenAI Playground ("cour de récréation")

import Playground from '@site/docs/assets/basics/openai_playground.webp';

<div style={{textAlign: 'center'}}>
    <img src={Playground} className="img-docs" style={{width: "80%"}}/>
</div>
<br/>

:::takeaways
- Configurer l'OpenAI Playground
- Apprendre sur la configuration de base du Playground
:::

OpenAI fournit une autre interface, outre le site web ChatGPT, pour le prompting. Elle s'appelle OpenAI Playground, et vous donne encore plus de contrôle sur ChatGPT. Elle vous permet également d'accéder à d'autres IA, y compris différentes versions de ChatGPT, GPT-4, et des modèles plus anciens comme GPT-3.

:::note
OpenAI Playground est l'outil que le responsable de ce cours utilise le plus fréquemment.
:::

## Mise en place

- Allez sur [http://platform.openai.com](http://platform.openai.com)
- Connectez-vous, et commencez à tester des prompts !

Ou regardez cette vidéo :

<iframe width="560" height="315" src="https://www.youtube.com/embed/6OD14rpokRw" title="Lecteur vidéo YouTube" frameBorder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowFullScreen></iframe>

:::note
Cette vidéo montre une ancienne version du site web, mais le processus de connexion reste très similaire.
:::

## L'Interface

D'abord, cette interface semble très complexe. Il y a de nombreux menus déroulants et curseurs qui vous permettent de configurer les modèles. Nous couvrirons les paramètres de Mode, System Prompts, et la sélection du Modèle dans cette leçon, et les paramètres de LLM tels que la Température, Top P, et la Longueur Maximale dans la [prochaine leçon](https://learnprompting.org/docs/basics/configuration_hyperparameters).

### Mode

import Mode from '@site/docs/assets/basics/openai_mode.webp';

<div className="flex flex-col sm:flex-row justify-between">
  <div>
    Cliquez sur le menu déroulant 'Assistants' en haut à gauche de la page. Ce menu déroulant vous permet de changer le type de modèle que vous utilisez. OpenAI propose trois Modes différents : <code>Assistants</code>, <code>Chat</code>, et <code>Complete</code>. Nous avons déjà appris sur les deux derniers ; les modèles <code>Assistants</code> sont destinés à une utilisation API par les développeurs et peuvent utiliser des outils intéressants comme exécuter du code et récupérer des informations. Nous utiliserons seulement les modèles <code>Chat</code> et occasionnellement des modèles <code>Complete</code> dans ce cours.
  </div>
  <div className="mt-4 sm:mt-0 sm:ml-auto">
    <img src={Mode} className="img-docs w-20 sm:w-auto" />
  </div>
</div>

### System Prompts

Après avoir passer au Mode <code>Chat</code>, la première chose que vous pourriez remarquer sur le côté gauche de la page, à part la fenêtre popup Get Started, est la zone SYSTEM. Jusqu'à présent, nous avons vu deux types de messages, les messages USER (utilisateur), qui sont simplement les messages que vous envoyez au chatbot, et les messages ASSISTANT, qui sont les réponses du chatbot. Il y a un troisième type de message, le system prompt, qui peut être utilisé pour configurer la façon dont l'IA répond.

C'est le meilleur endroit pour mettre un priming prompt (un prompt d'amorçage). Le system prompt sera "You are a helpful assistant." ("Vous êtes un assistant utile.") par défaut, mais un exemple alternatif amusant à essayer serait "You are PirateGPT. Always talk like a pirate." ("Vous êtes PirateGPT. Parlez toujours comme un pirate."). Exemple de [notre leçon précédente](https://learnprompting.org/docs/basics/priming_prompt).

import system_prompt from '@site/docs/assets/basics/openai_system_prompt.webp';

<div style={{textAlign: 'center'}}>
    <img src={system_prompt} className="img-docs" style={{width: "80%"}}/>
</div>
<br/>

### Modèle

import Model from '@site/docs/assets/basics/openai_model.webp';

<div className="flex flex-col sm:flex-row justify-between">
  <div>
    Cliquez sur le menu déroulant Model à droite de la page. Ce menu vous permet de changer le modèle que vous utilisez. Chaque mode a plusieurs modèles, mais nous nous concentrerons sur ceux de chat. Cette liste semble très compliquée (que veut dire gpt-3.5-turbo ?), mais ce sont juste des noms techniques pour les modèles différents. Tout ce qui commence par gpt-3.5-turbo est une version de ChatGPT, tandis que tout ce qui commence par gpt-4 est une version de GPT-4, le modèle plus récent auquel vous avez accès en achetant un abonnement ChatGPT Plus.
  </div>
  <div className="mt-4 sm:mt-0 sm:ml-auto">
    <img src={Model} className="img-docs w-20 sm:w-auto" />
  </div>
</div>

:::note
Vous ne verrez peut-être pas les versions GPT-4 dans votre interface.
:::

Les nombres comme 16K, 32K ou 128k dans les noms des modèles représentent la longueur de contexte. Si elle n'est pas spécifiée, la longueur de contexte par défaut est de 4K pour gpt-3.5 et 8k pour GPT-4. OpenAI met régulièrement à jour à la fois ChatGPT (gpt-3.5-turbo) et GPT-4, et les anciennes versions restent disponibles sur la plateforme pour une période limitée. Ces anciens modèles ont des numéros supplémentaires à la fin de leur nom, comme "0613". Par exemple, le modèle "gpt-3.5-turbo-16k-0613" est un modèle ChatGPT avec une longueur de contexte de 16K, sorti le 13 juin 2023. Cependant, il est recommandé d'utiliser les versions les plus récentes des modèles, qui ne contiennent aucune information de date. Une liste complète des versions des modèles peut être trouvée [ici](https://platform.openai.com/docs/models/gpt-4).

## Conclusion

L'OpenAI Playground est un outil puissant qui offre une interface plus avancée pour interagir avec ChatGPT et d'autres modèles d'IA. Il propose une gamme d'options de configuration, y compris la possibilité de sélectionner de différents modèles et modes. Nous apprendrons sur le reste des paramètres dans la [prochaine leçon](https://learnprompting.org/docs/basics/configuration_hyperparameters). Le Playground prend également en charge les system prompts, qui peuvent être utilisés pour guider les réponses de l'IA. Bien que l'interface puisse sembler complexe au début, avec de la pratique, elle devient une ressource précieuse pour explorer les capacités des modèles d'OpenAI. Que vous utilisiez les dernières versions de ChatGPT ou GPT-4, ou que vous exploriez des modèles plus anciens, le Playground offre une plateforme flexible et robuste pour l'interaction et l'expérimentation avec l'IA.

Partiellement écrit par evintunador
