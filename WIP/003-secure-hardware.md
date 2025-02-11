# Assumptions

 * SE "secure element" chips are by design difficult to inspect.
 * Sub 30nm chip fabrication will become ubiquitous.
 * Development should move toward open secure wallet hardware.

# Secure Element Containment Protocol

This is one proposal or recommendation for secure hardware design through the
distinction of open and closed components.

 * There are two types of elements in a secure design: the open source hardware
   component, and one or more SE components. We can think of these as two
   actors: one open, the other closed.

 * The assumption is that the open component can and will become mature over
   time, with a final state of provable completeness; and the closed component
   will also mature over time but have different priorities. For example part of
   the security goal is that the open components are probabilistically audited
   at the circuitry level, while a perfect closed SE component(s) may not be
   auditable by forensic inspection at all.

 * We assume that the closed SE component may contain arbitrary malicious
   circuitry; for example sub nanometer components hidden in a larger 25nm
   frame. The goal of the open component is to isolate the closed SE component
   such that arbitrary behavior can be tolerated.

 * It is NOT safe to expose the secure element to external interfaces. That is,
   the closed SE component may be compromised and may be conducting a
   man-in-the-middle attack upon the open component.

 * The usage of the closed SE component must be minimized as much as
   reasonable. For example, the open component could be designed so that it
   only requires of the closed SE component to hold a private key and to
   produce a signature for any input. The open component would still verify the
   resulting signature before emitting it. If this were the design of your
   hardware wallet, you would be less concerned about your secret leaking,
   because the closed SE component couldn't leak it even if it wanted to.

 * We should assume as our security threat model the cooperation of mobile
   device manufacturers AND SE component manufacturers. For example both could
   be coerced by a tyrannical administration under gag order to support a key
   extraction exploit for targeted individuals. If such an exploit were to
   affect a significant portion of the population it could prove existential to
   the crypto movement itself, at least for a time.

 * TODO: describe probabilistic auditing of open hardware.

 * TODO: describe example threat model where compromised information is
   stenographically injected into the usual expected payload, such as frame or
   user input data.

# USB Inspection Middleware

This is a separate proposal for an industry common standard.

Currently we plug in a hardware wallet directly into the computer by USB, and
we assume that the hardware wallet and computer are only interacting in the way
that we expect. But enforcing this security assumption isn't easy without the
aforementioned open-closed framework.

We can create another type of separation at the device level to introduce
additional security. A common USB device that sits between the computer and the
hardware wallet, and helps inspect transaction messages and checks signatures
for correctness, so that your hardware wallet transactions can be secure today,
even under the extreme threat model where both the computer as well as the
hardware wallets are compromised.

An open competitive market of compatible inspection devices would help bridge
the "big security gap" of crypto while more wallets become secure by virtue of
the "SE containment protocol". 
