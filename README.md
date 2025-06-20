// Bare Bliss Cleaning Co. - Topless Cleaning Service Website (React + Tailwind)

import React from "react";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";

export default function HomePage() {
  return (
    <div className="min-h-screen bg-black text-white font-sans">
      {/* Navigation Bar */}
      <header className="sticky top-0 z-50 bg-black border-b border-gray-800 flex justify-between items-center p-4">
        <h1 className="text-2xl font-bold text-gold">Bare Bliss</h1>
        <nav className="space-x-4 text-white">
          <a href="#" className="hover:text-gold">Home</a>
          <a href="#about" className="hover:text-gold">About</a>
          <a href="#services" className="hover:text-gold">Services</a>
          <a href="#pricing" className="hover:text-gold">Pricing</a>
          <a href="#gallery" className="hover:text-gold">Gallery</a>
          <a href="#contact" className="hover:text-gold font-semibold">Book Now</a>
        </nav>
      </header>

      {/* Hero Section */}
      <section className="bg-[url('/hero-image.jpg')] bg-cover bg-center h-[80vh] flex items-center justify-center">
        <div className="bg-black bg-opacity-60 p-10 rounded-2xl text-center max-w-xl">
          <h2 className="text-4xl md:text-5xl font-bold mb-4">Luxury Cleaning with a Sensual Twist</h2>
          <p className="mb-6 text-lg">Topless cleaners that leave your home spotless and your day unforgettable.</p>
          <Button className="bg-gold text-black text-lg px-6 py-3 rounded-2xl hover:scale-105">Book Your Experience</Button>
        </div>
      </section>

      {/* Services Preview */}
      <section id="services" className="py-16 px-4 bg-gray-900 text-center">
        <h3 className="text-3xl font-semibold text-gold mb-8">Our Signature Packages</h3>
        <div className="grid md:grid-cols-3 gap-6 max-w-6xl mx-auto">
          {[
            { title: "Basic Bliss", desc: "1 topless cleaner. Quick clean-up for small spaces." },
            { title: "Gentleman’s Deluxe", desc: "2 cleaners, deeper clean, optional light dance/music." },
            { title: "Executive Indulgence", desc: "2 cleaners, champagne option, custom themes." }
          ].map((service) => (
            <Card key={service.title} className="bg-black border-gold border text-white">
              <CardContent className="p-6">
                <h4 className="text-2xl font-bold mb-2 text-gold">{service.title}</h4>
                <p>{service.desc}</p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Call to Action */}
      <section className="py-12 bg-gold text-black text-center">
        <h3 className="text-3xl font-semibold mb-4">Discretion. Elegance. Bliss.</h3>
        <p className="mb-6">Book now and experience cleaning with a luxurious touch.</p>
        <Button className="bg-black text-gold text-lg px-6 py-3 rounded-2xl hover:scale-105">Book Now</Button>
      </section>

      {/* Footer */}
      <footer className="bg-black text-center text-gray-500 p-6 text-sm">
        © 2025 Bare Bliss Cleaning Co. | Topless Cleaning Services | All Rights Reserved
      </footer>
    </div>
  );
}
