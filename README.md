import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

export default function PobladoRP() {
  return (
    <div className="min-h-screen bg-gradient-to-b from-black via-neutral-900 to-black text-white">
      {/* HERO */}
      <section className="flex flex-col items-center justify-center text-center py-28 px-6">
        <motion.h1
          initial={{ opacity: 0, y: -20 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.6 }}
          className="text-5xl md:text-7xl font-bold mb-6"
        >
          Poblado Roleplay
        </motion.h1>
        <p className="text-lg text-neutral-300 max-w-2xl">
          Vive la mejor experiencia Roleplay en SA-MP. Sistema único, economía realista y comunidad activa.
        </p>
        <div className="mt-8 flex gap-4">
          <Button className="text-lg px-6 py-4">JUGAR AHORA</Button>
          <Button variant="outline" className="text-lg px-6 py-4">DISCORD</Button>
        </div>
      </section>

      {/* FEATURES */}
      <section className="grid md:grid-cols-3 gap-6 px-8 pb-20">
        {["Inventario estilo FiveM", "Sistema de bandas", "Economía realista"].map((f, i) => (
          <motion.div
            key={i}
            initial={{ opacity: 0, y: 20 }}
            whileInView={{ opacity: 1, y: 0 }}
            transition={{ delay: i * 0.2 }}
          >
            <Card className="bg-neutral-900 border-neutral-800 rounded-2xl shadow-lg">
              <CardContent className="p-6 text-center">
                <h3 className="text-xl font-semibold">{f}</h3>
                <p className="text-neutral-400 mt-2">
                  Disfruta de sistemas exclusivos diseñados para una experiencia RP única.
                </p>
              </CardContent>
            </Card>
          </motion.div>
        ))}
      </section>

      {/* SERVER INFO */}
      <section className="text-center pb-20">
        <h2 className="text-3xl font-bold mb-4">Información del Servidor</h2>
        <p className="text-neutral-400">IP: 127.0.0.1:7777</p>
        <p className="text-neutral-400">Modo: Roleplay</p>
        <p className="text-neutral-400">Jugadores Online: 120 / 500</p>
      </section>

      {/* FOOTER */}
      <footer className="text-center py-8 border-t border-neutral-800 text-neutral-500">
        © 2026 Poblado Roleplay - Todos los derechos reservados.
      </footer>
    </div>
  );
}
