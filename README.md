import React from "react";

const properties = [
  {
    id: 1,
    address: "54 North St, Douglas, MA 01516",
    price: "$589,900",
    bedrooms: 3,
    bathrooms: 2,
    size: "1,788 sqft",
    lot: "0.63 acre",
    description: "Charming single-family home with spacious interiors and a beautiful yard.",
    image: "https://via.placeholder.com/400x250"
  },
  {
    id: 2,
    address: "21 Elm St, Worcester, MA 01609",
    price: "$475,000",
    bedrooms: 4,
    bathrooms: 3,
    size: "2,100 sqft",
    lot: "0.50 acre",
    description: "Modern colonial-style home in the heart of Worcester with newly renovated kitchen.",
    image: "https://via.placeholder.com/400x250"
  },
  {
    id: 3,
    address: "102 Main St, Andover, MA 01810",
    price: "$749,000",
    bedrooms: 5,
    bathrooms: 4,
    size: "3,000 sqft",
    lot: "1 acre",
    description: "Elegant estate with large living spaces and a spacious backyard ideal for entertaining.",
    image: "https://via.placeholder.com/400x250"
  }
];

function App() {
  return (
    <div style={{ padding: '2rem', fontFamily: 'Arial, sans-serif' }}>
      <h1 style={{ fontSize: '2.5rem', marginBottom: '1rem' }}>Sonia Connolly Real Estate</h1>
      <p style={{ marginBottom: '2rem', color: '#666' }}>
        Your Trusted Partner in Massachusetts Real Estate
      </p>

      <div style={{ display: 'grid', gap: '1.5rem', gridTemplateColumns: 'repeat(auto-fit, minmax(300px, 1fr))', marginBottom: '3rem' }}>
        {properties.map((property) => (
          <div key={property.id} style={{ borderRadius: '16px', boxShadow: '0 4px 8px rgba(0,0,0,0.1)', overflow: 'hidden', backgroundColor: '#fff' }}>
            <img src={property.image} alt={property.address} style={{ width: '100%', height: '200px', objectFit: 'cover' }} />
            <div style={{ padding: '1rem' }}>
              <h2 style={{ fontSize: '1.25rem', marginBottom: '.5rem' }}>{property.address}</h2>
              <p style={{ color: '#2e7d32', fontWeight: 'bold', marginBottom: '.5rem' }}>{property.price}</p>
              <p style={{ fontSize: '0.9rem', color: '#555', marginBottom: '.5rem' }}>
                {property.bedrooms} Beds | {property.bathrooms} Baths | {property.size} | Lot: {property.lot}
              </p>
              <p style={{ fontSize: '0.85rem', color: '#777' }}>{property.description}</p>
            </div>
          </div>
        ))}
      </div>

      <div style={{ maxWidth: '600px', margin: '0 auto', padding: '2rem', backgroundColor: '#fff', borderRadius: '16px', boxShadow: '0 4px 12px rgba(0,0,0,0.1)' }}>
        <h2 style={{ fontSize: '1.75rem', marginBottom: '1rem' }}>Contact Sonia Connolly</h2>
        <p style={{ marginBottom: '1rem', color: '#555' }}>
          Have a question? Get in touch below or message me on{" "}
          <a href="https://www.facebook.com/share/16LmAneaAU/" target="_blank" rel="noopener noreferrer" style={{ color: '#1a73e8', textDecoration: 'underline' }}>
            Facebook
          </a>.
        </p>
        <form style={{ display: 'flex', flexDirection: 'column', gap: '1rem' }}>
          <input type="text" placeholder="Your Name" required style={{ padding: '.75rem', borderRadius: '8px', border: '1px solid #ccc' }} />
          <input type="email" placeholder="Your Email" required style={{ padding: '.75rem', borderRadius: '8px', border: '1px solid #ccc' }} />
          <textarea placeholder="Your Message" rows={5} required style={{ padding: '.75rem', borderRadius: '8px', border: '1px solid #ccc' }} />
          <button type="submit" style={{ padding: '.75rem', borderRadius: '8px', backgroundColor: '#1a73e8', color: '#fff', border: 'none', cursor: 'pointer' }}>
            Send Message
          </button>
        </form>
      </div>
    </div>
  );
}

export default App;
