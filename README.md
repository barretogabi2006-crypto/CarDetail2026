// Site-Limpeza-Carros.jsx
// React single-file component (Tailwind CSS required)
// Como usar:
// 1) Coloca este ficheiro num projeto React com Tailwind configurado (create-react-app + Tailwind, Next.js, ou Vite).
// 2) Edita as variáveis `BUSINESS_NAME`, `PHONE` e as imagens.
// 3) Para publicar rapidamente: Vercel ou Netlify a partir de um repositório GitHub.

import React from 'react';

const BUSINESS_NAME = 'Cardetail';
const PHONE = '+351935949961'; // substitui pelo teu número
const WHATSAPP_LINK = `https://wa.me/${PHONE.replace(/[^0-9]/g, '')}?text=Ol%C3%A1%2C%20gostaria%20de%20saber%20mais%20sobre%20a%20limpeza%20do%20meu%20carro`;

export default function CarWashLanding() {
  return (
    <div className="min-h-screen bg-gray-50 text-gray-900 font-sans">
      <header className="bg-white shadow">
        <div className="max-w-5xl mx-auto px-6 py-6 flex items-center justify-between">
          <h1 className="text-2xl font-extrabold">{BUSINESS_NAME}</h1>
          <nav className="hidden md:flex gap-6 items-center">
            <a href="#servicos" className="hover:underline">Serviços</a>
            <a href="#galeria" className="hover:underline">Galeria</a>
            <a href="#precos" className="hover:underline">Preços</a>
            <a href="#contacto" className="btn-primary inline-flex items-center px-4 py-2 rounded-full">Contactar</a>
          </nav>
          <div className="md:hidden">
            <a href={WHATSAPP_LINK} target="_blank" rel="noreferrer" className="inline-block px-3 py-2 bg-green-500 text-white rounded-lg">WhatsApp</a>
          </div>
        </div>
      </header>

      <main className="max-w-5xl mx-auto px-6 py-12">
        {/* Hero */}
        <section className="grid md:grid-cols-2 gap-8 items-center">
          <div>
            <h2 className="text-4xl font-extrabold leading-tight">Limpeza de carros profissional, rápida e cuidada</h2>
            <p className="mt-4 text-lg text-gray-600">Lavagem exterior, limpeza interior profunda, polimento e tratamentos de estofos — preços claros e marcação por WhatsApp.</p>

            <div className="mt-6 flex gap-3">
              <a href="#precos" className="inline-block bg-blue-600 text-white px-5 py-3 rounded-lg font-medium">Ver preços</a>
              <a href={WHATSAPP_LINK} target="_blank" rel="noreferrer" className="inline-block border border-gray-300 px-5 py-3 rounded-lg">Marcar via WhatsApp</a>
            </div>

            <ul className="mt-8 grid grid-cols-1 sm:grid-cols-2 gap-3 text-sm text-gray-700">
              <li>✅ Produtos de qualidade</li>
              <li>✅ Entrega rápida</li>
              <li>✅ Opções ecológicas</li>
              <li>✅ Tratamentos anti-manchas</li>
            </ul>
          </div>

          <div className="rounded-xl overflow-hidden shadow-lg">
            <img src="https://images.unsplash.com/photo-1542362567-b07e54358753?auto=format&fit=crop&w=1200&q=60" alt="car-cleaning" className="w-full h-72 object-cover" />
          </div>
        </section>

        {/* Services */}
        

        {/* Pricing */}
        <section id="precos" className="mt-12">
          <h3 className="text-2xl font-bold">Preços rápidos</h3>
          <p className="text-gray-600 mt-2">Preços indicativos — o preço final depende do tamanho do veículo e do nível de sujidade. Peça orçamento por WhatsApp.</p>

          <div className="mt-6 grid sm:grid-cols-2 gap-4">
            <div className="p-6 bg-white rounded-xl shadow">
              <h4 className="font-semibold">Limpeza Geral</h4>
              <p className="text-3xl font-bold mt-2">€20</p>
              <p className="mt-2 text-sm text-gray-600">Interior: estofos, vidros e plásticos (tempo médio: 1h30).<br/>Exterior: lavagem, cera e vidros.</p>
              <a href={WHATSAPP_LINK} target="_blank" rel="noreferrer" className="mt-4 inline-block px-4 py-2 border rounded-lg">Pedir orçamento</a>
            </div>

            <div className="p-6 bg-white rounded-xl shadow">
              <h4 className="font-semibold">Limpeza Detalhada</h4>
              <p className="text-3xl font-bold mt-2">€40</p>
              <p className="mt-2 text-sm text-gray-600">Interior detalhado com máquina de vapor nos estofos e vidros, pincéis nos plásticos (tempo médio: até 3h).<br/>Exterior: lavagem detalhada e cera com duração até 6 meses.</p>
              <a href={WHATSAPP_LINK} target="_blank" rel="noreferrer" className="mt-4 inline-block px-4 py-2 border rounded-lg">Pedir orçamento</a>
            </div>
          </div>
        </section>

        {/* Gallery */}
        <section id="galeria" className="mt-12">
          <h3 className="text-2xl font-bold">Galeria</h3>
          <div className="mt-4 grid sm:grid-cols-2 lg:grid-cols-3 gap-4">
            {galleryImages.map((src, i) => (
              <div key={i} className="rounded-lg overflow-hidden shadow">
                <img src={src} alt={`gallery-${i}`} className="w-full h-44 object-cover" />
              </div>
            ))}
          </div>
        </section>

        {/* Contact / Booking */}
        <section id="contacto" className="mt-12 mb-20 grid md:grid-cols-2 gap-8 items-center">
          <div>
            <h3 className="text-2xl font-bold">Contacto & Marcação</h3>
            <p className="mt-2 text-gray-600">Envia mensagem por WhatsApp para marcar hora ou pedir orçamento personalizado.</p>

            <div className="mt-6 flex items-center gap-3">
              <a href={WHATSAPP_LINK} target="_blank" rel="noreferrer" className="inline-flex items-center px-5 py-3 rounded-full bg-green-500 text-white font-semibold">Enviar WhatsApp</a>
              <a href={`tel:${PHONE}`} className="inline-flex items-center px-4 py-2 rounded-full border">Ligar</a>
            </div>

            <ul className="mt-6 text-sm text-gray-700 space-y-2">
              <li>📍 Área de serviço: substituir pelo nome da tua cidade</li>
              <li>🕒 Horário: 09:00 — 19:00 (segunda a sábado)</li>
              <li>💳 Pagamento: Dinheiro, MB WAY, Transferência</li>
            </ul>
          </div>

          <div className="p-6 bg-white rounded-xl shadow">
            <h4 className="font-semibold">Resumo rápido</h4>
            <p className="mt-2 text-gray-600">Serviço selecionado: <strong>Lavagem Express</strong></p>
            <p className="mt-2 text-gray-600">Preço estimado: <strong>€15</strong></p>
            <a href={WHATSAPP_LINK} target="_blank" rel="noreferrer" className="mt-4 inline-block px-4 py-2 bg-blue-600 text-white rounded-lg">Confirmar via WhatsApp</a>
          </div>
        </section>

        {/* FAQ */}
        <section className="mt-6">
          <h3 className="text-2xl font-bold">Perguntas Frequentes</h3>
          <details className="mt-4 p-4 bg-white rounded-lg shadow">
            <summary className="font-medium">Como agendo uma limpeza?</summary>
            <p className="mt-2 text-gray-600">Envia mensagem pelo WhatsApp com modelo do carro, local e dia pretendido.</p>
          </details>

          <details className="mt-4 p-4 bg-white rounded-lg shadow">
            <summary className="font-medium">Quanto tempo demora?</summary>
            <p className="mt-2 text-gray-600">Depende do serviço: lavagem express 20–30 min; limpeza interior 45–90 min.</p>
          </details>
        </section>
      </main>

      <footer className="bg-white border-t">
        <div className="max-w-5xl mx-auto px-6 py-6 flex flex-col md:flex-row items-center justify-between text-sm text-gray-600">
          <div>© {new Date().getFullYear()} {BUSINESS_NAME}</div>
          <div className="flex items-center gap-4">
            <a href={WHATSAPP_LINK} target="_blank" rel="noreferrer">WhatsApp</a>
            <a href={`tel:${PHONE}`}>Telefone</a>
          </div>
        </div>
      </footer>
    </div>
  );
}

function ServiceCard({ title, price, desc }) {
  return (
    <div className="p-6 bg-white rounded-xl shadow hover:shadow-lg transition">
      <h4 className="font-semibold">{title}</h4>
      <p className="text-xl font-bold mt-2">{price}</p>
      <p className="mt-3 text-sm text-gray-600">{desc}</p>
      <a href="#contacto" className="mt-4 inline-block px-3 py-2 border rounded-lg">Marcar</a>
    </div>
  );
}

const galleryImages = [
  'https://images.unsplash.com/photo-1502877338535-766e1452684a?auto=format&fit=crop&w=800&q=60',
  'https://images.unsplash.com/photo-1503376780353-7e6692767b70?auto=format&fit=crop&w=800&q=60',
  'https://images.unsplash.com/photo-1523986371872-9d3ba2e2f642?auto=format&fit=crop&w=800&q=60',
  'https://images.unsplash.com/photo-1511919884226-9f4e6b6f56b7?auto=format&fit=crop&w=800&q=60',
  'https://images.unsplash.com/photo-1511988617509-a57c8a288659?auto=format&fit=crop&w=800&q=60',
  'https://images.unsplash.com/photo-1503376780353-7e6692767b70?auto=format&fit=crop&w=800&q=60'
];
