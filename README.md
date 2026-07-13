import Image from "next/image";
import WelcomeContent from "./WelcomeContent";

export default function LandingPage() {
  return (
    <div className="relative min-h-screen overflow-hidden">

      {/* Background Image */}
      <Image
        src="/images/landing-bg.jpg"
        alt="Landing Background"
        fill
        priority
        quality={100}
        className="object-cover"
      />

      {/* Blue Overlay */}
      <div
        className="absolute inset-0"
        style={{
          background: "rgba(81, 209, 244, 0.6)",
        }}
      ></div>

      {/* Optional gradient to make it look richer */}
      <div
        className="absolute inset-0"
        style={{
          background:
            "linear-gradient(rgba(0,120,215,0.18), rgba(0,120,215,0.18))",
        }}
      ></div>

      {/* Page Content */}
      <div className="relative z-10">
        <WelcomeContent />
      </div>

    </div>
  );
}
