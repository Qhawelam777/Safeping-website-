# Safeping-website-
import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { Input } from "@/components/ui/input"; import { Mail } from "lucide-react"; import Image from "next/image";

export default function SafePingLandingPage() { return ( <div className="min-h-screen bg-white text-gray-900"> <header className="bg-orange-200 p-6 text-center"> <h1 className="text-4xl font-bold mb-2">SafePing</h1> <p className="text-lg">Africa's first smart emergency alert and medical safety app</p> </header>

<section className="p-6 grid md:grid-cols-2 gap-6 items-center">
    <div>
      <h2 className="text-2xl font-semibold mb-4">Your safety. One tap away.</h2>
      <p className="mb-4">
        SafePing is a powerful mobile safety app designed for women, youth,
        and vulnerable groups in South Africa. It lets you instantly send your
        live location, medical profile, and emergency alert to loved ones or
        emergency responders at the tap of a button.
      </p>
      <ul className="list-disc list-inside space-y-1 text-sm">
        <li>Auto SMS alerts with your live location</li>
        <li>Upload health profile (conditions, blood type, etc.)</li>
        <li>Generate printable medical card</li>
        <li>Optional police/ambulance integration (coming soon)</li>
        <li>Offline QR for emergency use</li>
      </ul>
    </div>
    <div className="relative w-full h-96">
      <Image
        src="/safeping-preview.png"
        alt="App Preview"
        layout="fill"
        objectFit="contain"
        className="rounded-2xl shadow-xl"
      />
    </div>
  </section>

  <section className="p-6 text-center bg-orange-100">
    <h3 className="text-xl font-semibold mb-2">Get Early Access</h3>
    <p className="mb-4 text-sm">Join the waitlist and be the first to download the app when it's ready.</p>
    <form
      action="https://formspree.io/f/mnqepzwl"
      method="POST"
      className="max-w-md mx-auto flex gap-2"
    >
      <Input
        type="email"
        name="email"
        placeholder="Enter your email"
        required
        className="flex-1"
      />
      <Button type="submit" className="bg-orange-500 hover:bg-orange-600 text-white">
        <Mail className="w-4 h-4 mr-2" /> Join
      </Button>
    </form>
  </section>

  <footer className="bg-gray-900 text-white p-4 text-center text-xs">
    <p>
      &copy; 2025 Busisiwe Maphela. All rights reserved. Unauthorized use or reproduction of this material is prohibited.
    </p>
  </footer>
</div>

); }

